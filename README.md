# comp_grafica_ufrj - Ray Tracing

Este projeto implementa um ray tracer básico utilizado como trabalho para a disciplina EEL882 - Computação Gráfica do curso de Engenharia de Computação e Informação da Universidade Federal do Rio de Janeiro (UFRJ). Esse projeto faz uso da linguagem Python juntamente com bibliotecas populares como NumPy e Matplotlib. Siga as instruções abaixo para configurar o ambiente, instalar as dependências necessárias e executar o código em um notebook Jupyter.

Claro! Aqui está uma breve explicação sobre como o ray tracing funciona:

## O Que é Ray Tracing?

Ray tracing é uma técnica de renderização utilizada para gerar imagens tridimensionais realistas. Ele simula o comportamento físico da luz para calcular como os raios de luz interagem com os objetos em uma cena. Essa técnica é amplamente utilizada em gráficos de computador para criar imagens com efeitos de iluminação realistas, sombras e reflexões.

### Como o Ray Tracing Funciona?

1. **Lançamento de Raios**:
   - A partir da câmera (ponto de vista do observador), raios são lançados em direção a cada pixel na tela.
   - Cada raio segue uma linha reta até encontrar um objeto na cena.

2. **Interseção com Objetos**:
   - Para cada raio lançado, calcula-se se e onde ele intersecta os objetos na cena (esferas, planos, etc.).
   - Isso envolve resolver equações matemáticas que descrevem as superfícies dos objetos.

3. **Cálculo de Cor**:
   - Quando um raio intersecta um objeto, calcula-se a cor do ponto de interseção.
   - A cor é determinada pela combinação de várias componentes de iluminação:
     - **Luz ambiente**: Iluminação geral da cena.
     - **Luz difusa**: Luz direta que atinge o objeto.
     - **Luz especular**: Reflexões brilhantes na superfície do objeto.
     - **Reflexões e Refrações**: Raios secundários que refletem ou refratam no ponto de interseção, contribuindo para a cor final.

4. **Sombras e Reflexões**:
   - Para cada ponto de interseção, calcula-se se ele está na sombra, lançando um novo raio em direção à fonte de luz.
   - Reflexões são calculadas lançando novos raios na direção refletida e repetindo o processo de interseção.

5. **Recursão**:
   - O processo de lançar raios pode ser recursivo para simular múltiplas reflexões e refrações.
   - A profundidade máxima de recursão é geralmente limitada para evitar cálculos excessivos.

## Como executar o programa
### Pré-requisitos

- Python 3.7 ou superior
- `pip` (gerenciador de pacotes Python)

### Passos para Configuração

1. **Clone o Repositório**

   Se você ainda não clonou o repositório, faça isso agora:
   ```sh
   git clone https://github.com/FelipeVillela/comp_grafica_ufrj.git
   cd comp_grafica_ufrj
   ```

2. **Crie um Ambiente Virtual**

   Recomenda-se criar um ambiente virtual para evitar conflitos de dependências com outros projetos.
   ```sh
   python -m venv env
   ```

3. **Ative o Ambiente Virtual**

   - **No Windows**
     ```sh
     .\env\Scripts\activate
     ```
   - **No macOS/Linux**
     ```sh
     source env/bin/activate
     ```

4. **Instale as Dependências**

   Com o ambiente virtual ativado, instale as dependências necessárias.
   ```sh
   pip install numpy matplotlib jupyter
   ```

5. **Inicie o Jupyter Notebook**

   Inicie o servidor Jupyter para editar e executar o notebook.
   ```sh
   jupyter notebook
   ```

   O Jupyter será executado no navegador, que automaticamente irá abrir.
   
   Mais informações podem ser encontradas na [página inicial do Jupyter](https://jupyter.org/).

6. **Abra o Notebook**

   Com o jupyter aberto no navegador, vá até o diretório onde o projeto foi clonado no arquivo `main.ipynb` para abrir o notebook.

7. **Execute o Código**

   No notebook Jupyter, execute as células uma a uma para entender o funcionamento e gerar a imagem renderizada.

### Estrutura do Código

- **Célula 1**: Importação das bibliotecas necessárias.
- **Célula 2**: Definição de funções auxiliares para normalização de vetores, cálculo de reflexão e interseção de raios com esferas.
- **Célula 3**: Configuração inicial da cena, incluindo a câmera, iluminação e objetos.
- **Célula 4**: Função principal `render_scene` que realiza a renderização da cena.
- **Célula 5**: Salvamento da imagem renderizada em um arquivo PNG.

### Salvando a Imagem

A última célula do notebook salva a imagem renderizada em um arquivo PNG chamado `ray_traced_image.png`.

Abaixo está a imagem renderizada pelo ray tracer:

![Imagem Renderizada](./ray_traced_image.png)

#### Encerrando o Ambiente Virtual

Após terminar o trabalho no projeto, você pode desativar o ambiente virtual:
```sh
deactivate
```

---

Seguindo essas instruções, você deve conseguir configurar o ambiente e executar o código do ray tracing com sucesso. 