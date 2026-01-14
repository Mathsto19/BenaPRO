# BenaPRO – Ferramenta de Anotação para Biometria Neonatal

Ferramenta de anotação e inspeção desenvolvida para criar labels estruturados em datasets de biometria neonatal, com foco em consistência e controle de qualidade.

---

## Sobre o Projeto

O BenaPRO foi desenvolvido para resolver um problema crítico na pesquisa em biometria neonatal: a necessidade de anotar erros de forma estruturada e consistente em imagens de impressões digitais de recém-nascidos. A ferramenta permite identificar múltiplos tipos de erros simultaneamente (classificação multirrótulo), atribuir níveis de severidade e gerar datasets padronizados para treinamento de modelos de inteligência artificial.

---

## Funcionalidades Principais

- Classificação multirrótulo: identifique múltiplos erros em uma única imagem (ex.: desfoque + sujeira + posicionamento)
- Escala de severidade: avalie a gravidade de cada erro em uma escala de 1 a 5 estrelas
- Visualização multi-canal: visualize simultaneamente 4 representações da mesma digital (pré-processada, segmentação de cristas, vales e mapa de minúcias)
- Exportação estruturada: dados exportados em formato JSON com rastreabilidade completa (ID, dedo, data, erros)
- Catálogo de erros: sistema baseado em 9 categorias de erro padronizadas

---

## Catálogo de Erros

| Código | Categoria | Descrição |
|--------|-----------|-----------|
| E01 | Digital Escura | Excesso de pressão, cristas fundidas |
| E02 | Manchas na Digital | Resíduos ou descamação entre as cristas |
| E03 | Fiapos na Digital | Presença de fibras de tecido |
| E04 | Escâner Sujo | Sujeira na superfície do sensor |
| E05 | Digital Clara | Falta de pressão, cristas descontínuas |
| E06 | Dedo Fora da Área | Posicionamento incorreto no sensor |
| E07 | Fora de Foco | Movimento durante a captura |
| E08 | Sem Padrão Visível | Impossível identificar cristas |
| E09 | Segmentação Boa | Imagem adequada para uso biométrico |

---

## Tecnologias

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyQt](https://img.shields.io/badge/PyQt-41CD52?style=flat-square&logo=qt&logoColor=white)

- Python 3.10+
- PyQt6 – Interface gráfica
- OpenCV – Processamento de imagens
- NumPy – Manipulação de dados

---

## Como Usar

### 1. Carregar Imagens
- Selecione um pacote `.zip` contendo as imagens organizadas por ID e dedo
- O sistema carrega automaticamente os metadados (data, ID do paciente, dedo)

### 2. Anotar Erros
- Selecione múltiplos erros: marque todos os problemas presentes na imagem
- Avalie a severidade: atribua uma nota de 1 (leve) a 5 (crítico) para cada erro
- Visualize as 4 representações: use as diferentes visualizações para identificar problemas sutis

### 3. Exportar Dados
- As anotações são salvas automaticamente em formato JSON
- Cada registro inclui: arquivo, data, ID, dedo, lista de erros e timestamps

---

## Estrutura de Dados

```json
{
  "pacote": "2024-01.zip",
  "imagens": [
    {
      "arquivo": "5ededao.png",
      "data": "30/01/2024",
      "id": "act",
      "dedo": "5ededao",
      "erros": [
        {
          "nome": "Dedo Fora da Área",
          "descricao": "Parte da digital ficou fora da área de captura",
          "avaliacao": 2,
          "timestamp": "2025-08-09 11:14:09"
        }
      ]
    }
  ]
}
````

---

## Aplicação na Pesquisa

O BenaPRO foi desenvolvido para:

* Criar datasets consistentes para treinar modelos de deep learning
* Reduzir o ruído de rotulagem (label noise) em pesquisas de biometria
* Padronizar a avaliação de qualidade entre diferentes anotadores
* Gerar dados para sistemas de feedback em tempo real durante a coleta

Resultados: foram anotadas 1.019 imagens de 39 recém-nascidos, totalizando 2.135 rótulos individuais.

---

## Requisitos

* Sistema Operacional: Windows 10+ ou Linux Ubuntu 20.04+
* Python: 3.10 ou superior
* Memória RAM: 4 GB mínimo
* Espaço em disco: 100 MB para a ferramenta + espaço para imagens

---

## Suporte e Contato

Para dúvidas ou colaborações:

* Matheus Augusto — [matheusaugustooliveira@alunos.utfpr.edu.br](mailto:matheusaugustooliveira@alunos.utfpr.edu.br)

---

## Agradecimentos

Este projeto foi desenvolvido na UTFPR com apoio das seguintes instituições:

* CNPq – Suporte financeiro via bolsa de Iniciação Científica
* CAPES – Código de Financiamento 001
* InfantID – Parceria e colaboração técnica
* UTFPR – Campus Pato Branco – Infraestrutura e grupo de pesquisa em Biometria Neonatal

---

## Licença

Distribuição autorizada apenas para fins acadêmicos, científicos e de pesquisa. Uso comercial ou redistribuição sem permissão é proibido.
