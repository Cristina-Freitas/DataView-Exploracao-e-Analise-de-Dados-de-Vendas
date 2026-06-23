# DataView - Exploração e Análise de Dados de Vendas

Mini Projeto do Curso de Desenvolvedor(a) em IA para Análise Preditiva.

## Sobre o Projeto

O DataView é um projeto de Análise Exploratória de Dados (EDA) desenvolvido em Python utilizando Jupyter Notebook.

O objetivo do projeto é demonstrar, de forma prática, as principais etapas de um pipeline de análise de dados:

- Inspeção do dataset;
- Limpeza e tratamento dos dados;
- Detecção e tratamento de outliers;
- Criação de colunas derivadas;
- Cálculo de métricas agregadas;
- Segmentação de clientes;
- Estatísticas utilizando NumPy;
- Visualização gráfica dos dados;
- Exportação de resultados em CSV e JSON;
- Consolidação do dataset final.

---

## Objetivos de Aprendizagem

Este projeto aplica conceitos fundamentais de Python e Ciência de Dados, incluindo:

- Variáveis e tipos de dados;
- Operadores aritméticos, lógicos e relacionais;
- Estruturas condicionais (`if`, `elif`, `else`);
- Estruturas de repetição (`for`);
- Funções com parâmetros e retorno;
- Funções lambda;
- Funções reutilizáveis;
- Função de ordem superior (callback);
- Manipulação de arquivos CSV e JSON;
- Expressões regulares (`re`);
- Manipulação de datas com `datetime`;
- Estruturas Pandas (`Series` e `DataFrame`);
- Filtros e transformações;
- Agrupamentos com `groupby`;
- Operações NumPy;
- Operações vetorizadas;
- Broadcasting;
- Detecção e tratamento de outliers utilizando IQR;
- Visualizações com Matplotlib e Seaborn;
- Versionamento com Git e GitHub.

---

## O que o Projeto Analisa

O projeto realiza análises sobre um conjunto de dados de vendas contendo:

- Clientes;
- Produtos;
- Categorias;
- Regiões;
- Quantidade vendida;
- Preço unitário;
- Receita gerada.

As análises incluem:

- Receita total por mês;
- Receita por categoria;
- Receita por produto;
- Receita por região;
- Segmentação de clientes por nível de gasto;
- Distribuição de receitas;
- Comparação entre versões com e sem tratamento de outliers.

---

## Estrutura do Projeto

```text
DataView-Exploracao-e-Analise-de-Dados-de-Vendas
│
├── data
│   ├── raw
│   │   └── vendas.csv
│   │
│   ├── processed
│   │   ├── v1_com_outliers
│   │   │   └── vendas_v1.csv
│   │   │
│   │   └── v2_outliers_tratado
│   │       └── vendas_v2.csv
│   │
│   └── final
│       └── vendas_final.csv
│
├── notebooks
│   └── dataview.ipynb
│
├── outputs
│   ├── metricas_por_mes.csv
│   ├── segmentacao_clientes.csv
│   ├── estatisticas_gerais.json
│   └── graficos
│       ├── receita_por_mes.png
│       ├── top_produtos.png
│       └── dist_regiao.png
│
└── README.md
```

---

## Tecnologias Utilizadas

- Python 3.11+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Regex (`re`)
- Datetime
- JSON
- Git
- GitHub
- VS Code
- Jupyter Notebook

---

## Como Executar

### 1. Clonar o Repositório

```bash
git clone <url-do-repositorio>
```

### 2. Acessar a Pasta

```bash
cd DataView-Exploracao-e-Analise-de-Dados-de-Vendas
```

### 3. Instalar Dependências

```bash
pip install pandas numpy matplotlib seaborn
```

### 4. Abrir o Notebook

Abra o arquivo:

```text
notebooks/dataview.ipynb
```

### 5. Executar Todas as Células

Execute as células na ordem apresentada.

O notebook irá:

- Gerar o dataset inicial;
- Realizar a limpeza dos dados;
- Tratar outliers;
- Criar métricas;
- Gerar gráficos;
- Exportar arquivos CSV e JSON;
- Salvar o dataset final.

---

## Tratamento dos Dados

Durante a etapa de limpeza foram realizados:

- Remoção de datas inválidas;
- Remoção de registros com valores nulos em colunas críticas;
- Padronização de textos utilizando expressões regulares;
- Conversão da coluna de datas para datetime;
- Detecção de outliers utilizando o método IQR.

---

## Versão Escolhida para o Dataset Final

### Versão utilizada

```text
v2_outliers_tratado
```

### Justificativa

A versão v2_outliers_tratado foi escolhida a partir da RF04 porque, após a limpeza geral da RF03, foram identificados 6 registros outliers pelo método IQR na coluna receita_total.

Como esses valores extremos poderiam distorcer as métricas agregadas, a segmentação de clientes, as estatísticas e os gráficos, optou-se por seguir com a base v2 nas etapas seguintes do projeto.

A versão v1_com_outliers foi mantida em data/processed para consulta e comparação, mas a versão v2 foi utilizada como base da análise principal e do dataset final.

---

## Principais Resultados Obtidos

- Receita total calculada por mês;
- Ranking dos produtos com maior faturamento;
- Receita consolidada por categoria;
- Receita consolidada por região;
- Segmentação de clientes em Bronze, Prata e Ouro;
- Estatísticas descritivas utilizando NumPy;
- Exportação dos resultados em CSV e JSON;
- Geração automática de gráficos em PNG.

---

## Conclusão

A análise exploratória permitiu identificar padrões relevantes no conjunto de dados de vendas.

Os produtos Tablet e Smartphone apresentaram as maiores receitas, enquanto a categoria Celulares concentrou o maior volume financeiro do dataset.

A segmentação de clientes mostrou predominância do segmento Ouro, indicando concentração significativa da receita em parte da base de clientes.

Durante o tratamento dos dados foram removidos registros com datas inválidas, valores nulos e outliers identificados pelo método IQR. Por esse motivo, a versão v2 foi escolhida como base para a análise final e para a geração do dataset consolidado.

O projeto demonstrou a aplicação prática de técnicas de limpeza, transformação, agregação, visualização e exportação de dados utilizando Python e as principais bibliotecas de análise de dados.

---

## Autor

Cristina Freitas

Projeto desenvolvido para o curso de Desenvolvimento de IA para Análise Preditiva do programa SCTEC.