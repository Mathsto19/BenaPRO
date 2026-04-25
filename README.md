# BENAPRO - Repositorio Oficial

Bem-vindo ao **BENAPRO**, um projeto voltado para rotulagem, inspecao e padronizacao de dados de biometria neonatal, com foco em impressoes digitais de recem-nascidos.

Este repositorio reune:
- **Aplicativo executavel (Windows)** para uso direto em campo/laboratorio
- **Codigo fonte em Python** para desenvolvimento, manutencao e pesquisa

---

## Sobre o Projeto

O BENAPRO foi desenvolvido para resolver um gargalo importante na pesquisa em biometria neonatal: a falta de rotulagem estruturada e consistente da qualidade das digitais coletadas.

A ferramenta permite:
- classificacao multirrotulo (mais de um erro por imagem)
- avaliacao de severidade por erro (1 a 5)
- visualizacao de multiplas representacoes da mesma digital
- exportacao rastreavel para formacao de datasets

Com isso, o projeto apoia estudos de inteligencia artificial para analise de qualidade, alinhamento e reconhecimento biometrico neonatal.

---

## Estrutura do Repositorio

```text
BENAPRO/
|-- Aplicativo/
|   |-- README.md
|-- Codigo Fonte/
|   |-- BenaPRO.py
|   |-- Requeriments.txt
|   |-- README.md
|   |-- Complementos/
|   |-- Exemplos/
|   `-- Fotos/
|-- LICENSE
`-- README.md
```

---

## Componentes

### 1. Aplicativo

Contem a versao empacotada para uso no Windows, sem necessidade de preparar ambiente Python manualmente.

Manual especifico:
- `Aplicativo/README.md`

### 2. Codigo Fonte

Contem a implementacao principal em Python para execucao, ajuste e evolucao do projeto.

Arquivos principais:
- `Codigo Fonte/BenaPRO.py`
- `Codigo Fonte/Requeriments.txt`
- `Codigo Fonte/README.md`

---

## Funcionalidades Principais

- **Carregamento por ZIP**: leitura de pacotes de imagens para analise sequencial
- **Visualizacao avancada**: zoom, arraste e filtros (normal, invertido, contraste, etc.)
- **Camadas RGBA**: alternancia entre canais para apoio tecnico na inspecao
- **Catalogo de erros**: cadastro/edicao de tipos de erro e descricoes
- **Avaliacao por severidade**: notas de 1 a 5 para cada erro selecionado
- **Exportacao estruturada**: salvamento das anotacoes em JSON para uso cientifico

---

## Catalogo de Erros (Padrao)

| Codigo | Categoria | Descricao |
|--------|-----------|-----------|
| E01 | Digital Escura | Excesso de pressao, cristas fundidas |
| E02 | Manchas na Digital | Residuos ou descamacao entre as cristas |
| E03 | Fiapos na Digital | Presenca de fibras de tecido |
| E04 | Escaner Sujo | Sujeira na superficie do sensor |
| E05 | Digital Clara | Falta de pressao, cristas descontinuas |
| E06 | Dedo Fora da Area | Posicionamento incorreto no sensor |
| E07 | Fora de Foco | Movimento durante a captura |
| E08 | Sem Padrao Visivel | Impossivel identificar cristas |
| E09 | Segmentacao Boa | Imagem adequada para uso biometrico |

---

## Como Executar

### Opcao A - Usar o aplicativo (Windows)

1. Acesse a pasta do aplicativo.
2. Execute `BENAPRO.exe`.
3. Siga as instrucoes do manual em `Aplicativo/README.md`.

### Opcao B - Rodar pelo codigo fonte (Python)

1. Entre em `Codigo Fonte/`.
2. Instale as dependencias:

```bash
pip install -r Requeriments.txt
```

3. Execute o sistema:

```bash
python BenaPRO.py
```

---

## Saida de Dados

As anotacoes sao salvas em arquivo JSON estruturado, geralmente em:

```text
BENAPRO/resultado.json
```

Os registros podem incluir:
- arquivo analisado
- data
- identificador do paciente
- dedo/frame
- erros selecionados
- avaliacoes por erro
- timestamp da anotacao

---

## Requisitos Tecnicos

- Sistema operacional: Windows 10/11 (aplicativo) e ambiente Python para desenvolvimento
- Python: 3.10+
- Bibliotecas principais: PyQt6, OpenCV, NumPy
- RAM recomendada: 8 GB
- Espaco em disco: conforme volume de imagens e pacotes ZIP

---

## Impacto Cientifico

O BENAPRO contribui para:
- reducao de ruido de rotulagem em datasets biometricos
- padronizacao entre diferentes anotadores
- criacao de base confiavel para treinamento de modelos de IA
- melhoria de processos de controle de qualidade na coleta neonatal

---

## Suporte e Contato

Para duvidas, suporte tecnico ou colaboracoes:

- Matheus Augusto - [matheusaugustooliveira@alunos.utfpr.edu.br](mailto:matheusaugustooliveira@alunos.utfpr.edu.br)

---

## Agradecimentos

Este projeto foi desenvolvido na UTFPR com apoio das instituicoes:

- CNPq
- CAPES (Codigo de Financiamento 001)
- InfantID
- UTFPR - Campus Pato Branco

---

## Licenca

Distribuicao autorizada apenas para fins academicos, cientificos e de pesquisa.
Uso comercial ou redistribuicao sem permissao e proibido.
