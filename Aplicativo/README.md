# BENAPRO – Aplicativo para Rotulagem de Imagens Biométricas

## Sobre o BENAPRO

O BENAPRO é um aplicativo voltado para rotulagem, inspeção e avaliação de imagens biométricas, com foco em impressões digitais. A ferramenta permite carregar pacotes de imagens, analisar camadas específicas, registrar erros encontrados e atribuir avaliações para cada marcação.

Seu principal objetivo é organizar o processo de análise biométrica com rastreabilidade, padronização e registro estruturado dos resultados.

---

## Compatibilidade

| Sistema Operacional | Executável | Script Fonte |
|---------------------|------------|--------------|
| Windows 10/11       | `BENAPRO.exe` | `BenaPRO.py` |

---

## Como Utilizar o BENAPRO

### 1. Inicializando o Aplicativo

**No Windows:**
- Execute o arquivo `BENAPRO.exe` na pasta do aplicativo.
- Se houver bloqueio de segurança, clique em **Mais informações** e depois em **Executar assim mesmo**.

---

### 2. Carregamento de Imagens

- Clique em `Carregar ZIP`.
- Selecione um arquivo `.zip` com as imagens a serem avaliadas.
- O BENAPRO extrai o conteúdo e organiza a sequência de análise.
- Quando disponível no nome/estrutura dos arquivos, o sistema identifica automaticamente informações como data, ID, dedo e frame.

---

### 3. Navegação e Visualização

- Use os controles de navegação para avançar e voltar entre imagens.
- Também é possível navegar pelas setas do teclado (esquerda/direita).
- O contador de progresso indica imagens avaliadas e pendentes.
- A roda do mouse controla o zoom.
- Clique e arraste para mover a imagem quando ampliada.

---

### 4. Filtros e Camadas

No botão `Cores`, você pode aplicar diferentes modos de visualização:

- Normal
- Inverter cores
- Alto contraste
- Mais brilhante
- Mais escuro

Para imagens com quatro canais (RGBA), o BENAPRO permite alternar visualizações por camada usando os botões `1`, `2`, `3` e `4`:

- `1`: Calibrado/Alpha
- `2`: Segmentação de cristas
- `3`: Segmentação de vales
- `4`: Minúcias

Ao clicar novamente na camada ativa, a visualização retorna para a imagem original.

---

### 5. Registro de Erros

- Clique em `Personalizar Erros` para cadastrar, editar ou remover tipos de erro e suas descrições.
- Clique em `Erro` para selecionar os problemas encontrados na imagem atual.
- Cada erro selecionado deve ter descrição correspondente.

---

### 6. Avaliação

- Clique em `Avaliação` para abrir a janela de notas.
- Cada erro selecionado deve receber uma avaliação de 1 a 5 estrelas.
- O salvamento só é permitido quando todos os erros selecionados estiverem avaliados.

---

### 7. Salvando os Resultados

Após selecionar os erros e finalizar as avaliações:

1. Clique em `Salvar`.
2. O BENAPRO registra os dados no arquivo:

```text
BENAPRO/resultado.json
```

O arquivo de resultados pode incluir, entre outros campos:

- Nome do arquivo avaliado
- Data
- ID
- Dedo
- Erros selecionados
- Descrições
- Avaliações
- Horário da anotação

Após salvar, o sistema marca a imagem como avaliada e tenta avançar para a próxima pendente.

---

## Atalhos e Recursos Extras

- `Esc`: fecha o aplicativo.
- Setas esquerda/direita: navegação entre imagens.
- Clique no logo do CNPq: abre o manual interno do BENAPRO.
- Clique no logo da UTFPR: abre a página do projeto
  (`https://sites.google.com/view/utfprbiometria`).

---

## Requisitos Técnicos

- Sistema operacional: Windows 10 ou superior
- Memória RAM: 8 GB recomendados
- Armazenamento: espaço para extração dos arquivos `.zip` e gravação dos resultados
- Resolução de tela recomendada: 1920x1080

---

## Estrutura de Arquivos (Aplicativo)

📁 **BENAPRO/**  
├── `BENAPRO.exe` – Executável para Windows  
├── `Complementos/` – Arquivos de apoio do sistema  
├── `Fotos/` – Logos e imagens da interface  
├── `Exemplos/` – Arquivos de exemplo para teste  
├── `BENAPRO/` – Pasta de saída com `resultado.json`  
└── `README.md` – Manual do usuário

---

## Suporte

Em caso de dúvidas, sugestões ou problemas técnicos:

- E-mail: matheusaugustooliveira@alunos.utfpr.edu.br

---

## Licença

Este software é distribuído para fins acadêmicos, científicos e de pesquisa.
Uso comercial ou distribuição indevida não são permitidos sem autorização.

---

## Agradecimentos

Desenvolvido com apoio da Universidade Tecnológica Federal do Paraná (UTFPR) e do CNPq, para projetos de biometria e análise de impressões digitais.

