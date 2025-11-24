# 🎯 Tiro ao Alvo 🤘

> Um FPS (First-Person Shooter) frenético desenvolvido para rodar no navegador, combinando mecânicas clássicas, física 3D e trilha sonora imersiva.

## 📋 Objetivo do Projeto

O objetivo deste projeto é criar uma experiência completa de "Game Loop" utilizando tecnologias web modernas. O jogo desafia o jogador a:

* **Explorar cenários 3D** com movimentação livre e física de colisão.
* **Acertar alvos móveis** gerados proceduralmente dentro de um tempo limite (60s).
* **Gerenciar precisão e agilidade** utilizando controles padrão de FPS.
* **Competir no Ranking**, com pontuações salvas localmente baseadas em precisão e tempo restante.

## 🛠 Tecnologias Utilizadas

O projeto foi construído com uma stack moderna focada em performance e desenvolvimento ágil:

* **[Node.js](https://nodejs.org/):** Ambiente de execução.
* **[Vite](https://vitejs.dev/):** Build tool e servidor de desenvolvimento (HMR).
* **[Three.js (r167)](https://threejs.org/):** Biblioteca principal para renderização 3D.
* **Three.js Addons:**
    * `GLTFLoader`: Importação de mapas/modelos 3D.
    * `Octree` & `Capsule`: Sistema avançado de física e colisão espacial.
* **Web Audio API:** Manipulação de áudio e efeitos sonoros procedurais.
* **HTML5/CSS3:** Interface (HUD) e menus.

## 🎮 Controles

| Tecla | Ação |
| :---: | :--- |
| **W, A, S, D** | Mover o personagem |
| **ESPAÇO** | Pular |
| **MOUSE** | Mirar |
| **CLIQUE ESQ.** | Atirar |

## 🚀 Instalação e Execução

Siga os passos abaixo para rodar o projeto localmente utilizando `npm`.

### Pré-requisitos
Certifique-se de ter o **[Node.js](https://nodejs.org/)** instalado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/tiro-ao-alvo-doom.git](https://github.com/seu-usuario/tiro-ao-alvo-doom.git)
    cd tiro-ao-alvo-doom
    ```

2.  **Instale as dependências:**
    Este comando baixará o `three`, `vite` e outras bibliotecas listadas no `package.json`.
    ```bash
    npm install
    ```

3.  **Execute o servidor de desenvolvimento:**
    Inicie o projeto localmente.
    ```bash
    npm run dev
    ```

4.  **Jogue:**
    O terminal exibirá um link local (geralmente `http://localhost:5173/`). Clique nele ou cole no seu navegador para começar.

## ⚡ Principais Desafios Técnicos

Durante o desenvolvimento acadêmico deste projeto, a equipe superou os seguintes obstáculos:

1.  **Física com Octrees:**
    * *Desafio:* Implementar detecção de colisão precisa em mapas 3D complexos (com escadas e rampas) sem atravessar paredes.
    * *Solução:* Uso de **Octrees** para particionamento espacial da geometria do mapa combinado com **Capsule Geometry** para o corpo do jogador.

2.  **Geração Procedural de Alvos:**
    * *Desafio:* Fazer com que os alvos apareçam aleatoriamente ("spawn") dentro da área jogável, sem flutuar no infinito ou ficar presos dentro de paredes.
    * *Solução:* Cálculo dinâmico da *Bounding Box* do mapa carregado para definir os limites XYZ seguros para instanciar os objetos.

3.  **Gerenciamento de Áudio (Browser Policy):**
    * *Desafio:* Lidar com as restrições de "Autoplay" dos navegadores modernos.
    * *Solução:* Implementação de um manipulador de contexto de áudio que só libera a música e efeitos após a primeira interação física do usuário (clique).

## 👥 Equipe

Projeto desenvolvido pelo **Sexto Período** sob orientação do Professor **Tulio Gomes**.

* Rafael Florindo
* Luciano Junior
* Otavio Herdy
* Caua Vitor

---
*Desenvolvido para fins educacionais.*
