# Análise de Padrões Territoriais de Votação por meio de Clusterização

## 1. Sobre o projeto

Este projeto tem como objetivo identificar e analisar padrões territoriais de votação nas seções eleitorais brasileiras, utilizando técnicas de Ciência de Dados e Aprendizado de Máquina não supervisionado.

A análise utiliza dados eleitorais disponibilizados pelo Tribunal Superior Eleitoral (TSE), com foco na distribuição percentual dos votos de candidatos, votos em branco e votos nulos.

Por meio do algoritmo **K-Means**, busca-se agrupar seções eleitorais com características semelhantes, permitindo identificar diferentes perfis de comportamento eleitoral e compreender como esses padrões se distribuem territorialmente.

## 2. Base de dados

Os dados utilizados são provenientes do Tribunal Superior Eleitoral (TSE).

A base consolidada utilizada na modelagem contém:

- **499.205 seções eleitorais**;
- 499.205 chaves distintas, sem duplicidades;
- Ausência de valores nulos nas três variáveis utilizadas;
- Ausência de seções sem votos válidos.

As informações geográficas e administrativas, como UF, município, zona e seção eleitoral, foram preservadas para permitir a interpretação territorial dos agrupamentos.

## 3. Variáveis utilizadas

Para a construção dos agrupamentos, foram selecionadas três variáveis quantitativas:

| Variável | Descrição |
|---|---|
| `PERC_CANDIDATO_22` | Proporção de votos do candidato 22 em relação aos votos válidos. |
| `PERC_BRANCOS` | Proporção de votos em branco em relação ao total de votos registrados. |
| `PERC_NULOS` | Proporção de votos nulos em relação ao total de votos registrados. |

As variáveis foram selecionadas por representarem características distintas da distribuição dos votos nas seções eleitorais.

As informações de identificação territorial não foram utilizadas diretamente na formação dos clusters, sendo preservadas para análises posteriores.

## 4. Tecnologias e bibliotecas

O desenvolvimento foi realizado em Python, utilizando o ambiente Google Colab e as seguintes tecnologias:

- **PySpark:** processamento e manipulação dos dados em escala.
- **Pandas:** apoio à análise e organização dos resultados.
- **NumPy:** operações numéricas.
- **
