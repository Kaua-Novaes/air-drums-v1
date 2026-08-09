# 🥁 Bateria Virtual com OpenCV e Pygame

Uma bateria virtual controlada por **webcam**, desenvolvida em Python utilizando **OpenCV** para visão computacional e **Pygame** para reprodução dos sons.

O sistema identifica, em tempo real, objetos de cor vermelha — como a ponta de uma baqueta marcada com fita vermelha — e verifica quando eles atingem as regiões correspondentes às peças da bateria. Ao detectar um "toque", o som da peça é reproduzido automaticamente.

## 🎯 Funcionalidades

* 🎥 Detecção de objetos vermelhos em tempo real utilizando webcam
* 🥁 Simulação de diferentes peças de uma bateria
* 🔊 Reprodução de sons específicos para cada peça
* ⚡ Resposta em tempo real aos movimentos da baqueta
* 🖥️ Interface visual com as regiões de cada instrumento
* ⌨️ Tecla `ESC` para encerrar a aplicação

## 🧠 Tecnologias utilizadas

| Tecnologia   | Utilização                                   |
| ------------ | -------------------------------------------- |
| **Python 3** | Linguagem principal                          |
| **OpenCV**   | Captura da webcam e processamento de imagem  |
| **NumPy**    | Manipulação de dados e operações matemáticas |
| **Pygame**   | Reprodução dos sons da bateria               |

## 📂 Estrutura do projeto

```text
bateria_virtual/
│
├── sons/
│   ├── caixa.wav
│   ├── ximbau.wav
│   ├── tom1.wav
│   ├── prato.wav
│   └── surdo.wav
│
├── main.py
└── README.md
```

## ⚙️ Instalação

### 1. Clone o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd bateria_virtual
```

### 2. Instale as dependências

```bash
pip install opencv-python numpy pygame
```

### 3. Adicione os arquivos de áudio

Coloque os arquivos `.wav` correspondentes aos sons da bateria dentro da pasta `sons/`.

Exemplo:

```text
sons/
├── caixa.wav
├── ximbau.wav
├── tom1.wav
├── prato.wav
└── surdo.wav
```

## ▶️ Executando o projeto

Execute o arquivo principal:

```bash
python main.py
```

Uma janela será aberta utilizando a webcam para capturar os movimentos.

## 🎮 Como utilizar

1. Conecte e habilite sua webcam.
2. Coloque uma **fita vermelha** na ponta de uma baqueta, caneta ou objeto semelhante.
3. Execute o programa.
4. Posicione o objeto diante da câmera.
5. Mova o objeto até uma das regiões indicadas na tela.
6. Ao atingir uma região, o som correspondente será reproduzido.
7. Pressione **`ESC`** para encerrar a aplicação.

> 💡 Para obter melhores resultados, utilize uma fita vermelha com boa iluminação e evite outros objetos vermelhos no campo de visão da câmera.

## 🥁 Mapeamento dos instrumentos

| Posição aproximada `(x, y)` | Instrumento | Descrição             |
| --------------------------- | ----------- | --------------------- |
| `(781, 615)`                | Caixa       | Caixa da bateria      |
| `(950, 475)`                | Ximbau      | Hi-hat                |
| `(780, 335)`                | Tom 1       | Tom pequeno           |
| `(580, 335)`                | Prato       | Prato crash           |
| `(469, 535)`                | Surdo       | Surdo / bumbo lateral |

## 🔍 Como funciona

O funcionamento do projeto pode ser dividido em algumas etapas:

```text
Webcam
   ↓
Captura do frame
   ↓
Conversão para HSV
   ↓
Detecção da cor vermelha
   ↓
Identificação da posição do objeto
   ↓
Verificação da região atingida
   ↓
Reprodução do som correspondente
```

O **OpenCV** é responsável por analisar os frames capturados pela webcam e identificar os objetos vermelhos. A posição detectada é então comparada com as áreas definidas para cada instrumento.

Quando há uma colisão entre o objeto detectado e uma dessas áreas, o **Pygame** reproduz o arquivo de áudio associado ao instrumento.

## 🚀 Possíveis melhorias

Algumas funcionalidades que podem ser implementadas futuramente:

* 🎨 Suporte para múltiplas cores de rastreamento
* 🥁 Detecção simultânea das duas baquetas
* ✨ Animações ao atingir cada instrumento
* 🎚️ Configuração da sensibilidade da detecção
* 🔇 Redução de falsos positivos causados por ruídos da câmera
* 🎵 Adição de mais instrumentos e sons
* 🖥️ Interface gráfica para configuração das áreas da bateria
* 📊 Calibração automática das regiões de detecção

## 👨‍💻 Autor

**Kauã Novaes**

Projeto desenvolvido em **Python**, explorando conceitos de **visão computacional, processamento de imagens e reprodução de áudio em tempo real**.

---

🥁 **Feito com Python + OpenCV + Pygame**
