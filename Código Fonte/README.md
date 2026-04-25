# BenaPRO - Software para Rotulagem de Imagens Biométricas

## Bem-vindo ao BenaPRO

O BenaPRO é um software desenvolvido para auxiliar na rotulagem, inspeção e avaliação de imagens biométricas, com foco em impressões digitais. A ferramenta permite carregar conjuntos de imagens, visualizar camadas específicas, registrar erros encontrados e atribuir avaliações para cada marcação realizada.

O objetivo principal do programa é facilitar a organização das análises, mantendo um registro estruturado dos erros observados em cada imagem avaliada.

## Estrutura do Projeto

A pasta do projeto deve manter os arquivos e diretórios junto ao código fonte principal (`BenaPRO.py`):

- `BenaPRO.py`: código fonte principal do software.
- `Complementos`: contém arquivos complementares usados pelo programa.
- `Exemplos`: inclui arquivos de exemplo para teste, como pacotes `.zip` de imagens.
- `Fotos`: armazena as logos e imagens utilizadas na interface.
- `BENAPRO`: pasta criada e usada pelo sistema para salvar resultados, como `resultado.json`.
- `Requeriments.txt`: arquivo com as bibliotecas necessárias para executar o software.

## Instalação e Preparação

1. Baixe a pasta completa do projeto e mantenha a estrutura original de arquivos.
2. Instale o Python 3.10 ou superior.
3. Instale as dependências:

```bash
pip install -r Requeriments.txt
```

4. Execute o software:

```bash
python BenaPRO.py
```

## Como Utilizar o BenaPRO

### 1. Carregando as Imagens

- Clique em `Carregar ZIP`.
- Selecione um arquivo `.zip` contendo as imagens que serão avaliadas.
- O programa extrai os arquivos, organiza a lista de imagens e tenta identificar informações como data, ID, dedo e frame.

### 2. Navegação

- Use os botões de navegação na parte inferior da área de visualização para avançar ou voltar.
- Também é possível usar as setas do teclado para navegar entre as imagens.
- O contador indica o progresso e muda de cor conforme o arquivo atual já tenha sido avaliado ou ainda esteja pendente.

### 3. Visualização e Filtros

- O botão `Cores` permite aplicar filtros de visualização:
  - Normal
  - Inverter cores
  - Alto contraste
  - Mais brilhante
  - Mais escuro

- A roda do mouse controla o zoom.
- Clique e arraste a imagem para mover a visualização quando ela estiver ampliada.

### 4. Camadas RGBA

Quando a imagem possuir quatro canais, o BenaPRO permite visualizar camadas separadas pelos botões `1`, `2`, `3` e `4`:

- `1`: Calibrado / Alpha
- `2`: Segmentação de cristas
- `3`: Segmentação de vales
- `4`: Minúcias

Ao clicar novamente na camada selecionada, o programa retorna para a imagem original.

### 5. Catálogo e Seleção de Erros

- Clique em `Personalizar Erros` para cadastrar, editar ou remover nomes e descrições de erros.
- Clique em `Erro` para selecionar os erros observados na imagem atual.
- Cada erro selecionado deve possuir uma descrição correspondente.

### 6. Avaliação

- Clique em `Avaliação` para abrir a janela de notas.
- Cada erro selecionado deve receber uma avaliação de 1 a 5 estrelas.
- O programa só permite salvar quando todos os erros selecionados estiverem avaliados.

### 7. Salvando os Resultados

- Clique em `Salvar` após selecionar e avaliar os erros.
- As informações são gravadas em:

```text
BENAPRO/resultado.json
```

O arquivo salva os dados por ZIP analisado, incluindo:

- Nome do arquivo avaliado
- Data
- ID
- Dedo
- Erros selecionados
- Descrições
- Avaliações
- Horário da anotação

Após salvar, o programa marca a imagem como avaliada e tenta avançar para a próxima pendente.

## Atalhos e Recursos Extras

- Clique no logo do CNPq para abrir o manual interno do BenaPRO.
- Clique no logo da UTFPR para acessar o site do projeto: https://sites.google.com/view/utfprbiometria
- A tecla `Esc` fecha o programa.
- As setas esquerda e direita navegam entre as imagens.

## Especificações Técnicas

### Requisitos Mínimos

- Sistema operacional: Windows 10 ou superior.
- Python: 3.10 ou superior.
- Memória RAM: 8 GB recomendados.
- Armazenamento: espaço suficiente para extração dos arquivos `.zip` e gravação dos resultados.

### Principais Bibliotecas

- PyQt6: interface gráfica e recursos multimídia.
- OpenCV: leitura e processamento das imagens.
- NumPy: suporte para manipulação de dados de imagem.

## Suporte e Contato

Em caso de dúvidas, sugestões ou problemas técnicos, entre em contato:

- **E-mail:** matheusaugustooliveira@alunos.utfpr.edu.br

## Licença

Este software é distribuído para fins acadêmicos, científicos e de pesquisa. O uso comercial ou indevido não é permitido sem autorização.

## Agradecimentos

Este projeto foi desenvolvido com apoio da Universidade Tecnológica Federal do Paraná (UTFPR) e do CNPq.
