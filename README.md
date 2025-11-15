# README — Análise do Dataset Housing California

## Visão Geral

Este repositório contém o *notebook* `housing_california.ipynb`, que realiza uma análise completa do clássico dataset **California Housing**. O objetivo é demonstrar um workflow de Ciência de Dados para **previsão de preços de imóveis**, incluindo análise exploratória, preparação de dados, engenharia de atributos, modelagem e avaliação.

---

## Sumário

1. Objetivo do notebook
2. Sobre o dataset
3. Estrutura do notebook
4. Como executar o projeto
5. Metodologia aplicada
6. Resultados esperados
7. Conclusões e interpretações
8. Melhorias sugeridas

---

## 1. Objetivo do notebook

* Realizar uma análise detalhada do dataset California Housing.
* Construir um modelo de regressão para prever o valor mediano das casas em diferentes localidades.
* Demonstrar pipeline completo: EDA → Pré-processamento → Modelagem → Validação → Interpretação.
* Criar visualizações claras e insights úteis que podem compor um portfólio profissional.

---

## 2. Sobre o dataset

* **Nome:** California Housing
* **Origem:** disponível no `sklearn.datasets.fetch_california_housing()`.
* **Tamanho:** ~20.000 linhas e 8 variáveis explicativas.
* **Atributos principais:**

  * `MedInc`: renda mediana
  * `HouseAge`: idade média das casas
  * `AveRooms`: média de cômodos
  * `AveBedrms`: média de dormitórios
  * `Population`: população
  * `AveOccup`: taxa média de ocupação
  * `Latitude`, `Longitude`
* **Alvo:** `MedHouseVal` — valor mediano das casas.

Dataset amplamente usado para comparação entre modelos de regressão.

---

## 3. Estrutura do notebook

O notebook está organizado nas seções:

1. **Imports e carregamento dos dados**
2. **Visão geral inicial** — `.head()`, `.info()`, `.describe()`
3. **EDA e visualizações** — histogramas, correlações, mapas de dispersão
4. **Limpeza e pré-processamento** — padronização, train-test split
5. **Engenharia de atributos** — combinações úteis (ex.: rooms_per_household)
6. **Modelagem** — regressão linear, árvores, random forest, gradient boosting
7. **Métricas de avaliação** — MAE, MSE, RMSE, R²
8. **Comparação dos modelos**
9. **Conclusões e próximos passos**

---

## 4. Como executar o projeto

### Requisitos

Instale todas as dependências:

```bash
pip install -r requirements.txt
```

### Execução

```bash
jupyter lab
```

Abra o arquivo `housing_california.ipynb` na pasta `notebooks/`.

---

## 5. Metodologia aplicada

* **EDA para entendimento dos padrões espaciais** (latitude/longitude influenciam fortemente o valor).
* **Padronização dos dados** quando necessário.
* **Divisão estratificada baseada em renda mediana**, caso utilizada.
* **Modelagem baseada em múltiplos algoritmos** e comparação objetiva.
* **Interpretação dos resultados** usando importância de features.

---

## 6. Resultados esperados

* Identificação clara dos fatores que mais impactam o preço das casas.
* Visualização do valor dos imóveis ao longo do mapa da Califórnia.
* Modelos com bom desempenho, especialmente *Random Forest Regressor* e *Gradient Boosting*, que costumam superar regressão linear.
* Relatório com métricas para cada modelo.

---

## 7. Conclusões e interpretações

* Renda mediana tende a ser o atributo mais importante na explicação dos preços.
* Localização geográfica influencia fortemente (efeito espacial).
* Modelos baseados em árvores normalmente oferecem melhor capacidade de captura de não-linearidades.
* A análise sugere potenciais estratégias para precificação e segmentação imobiliária.

---

## 8. Melhorias sugeridas

* Realizar busca de hiperparâmetros com GridSearch ou RandomizedSearch.
* Adicionar validação cruzada estratificada.
* Construir mapa geoespacial com Folium ou GeoPandas.
* Testar modelos mais avançados (XGBoost, LightGBM, CatBoost).
* Implementar pipeline do scikit-learn com persistência de modelo.

---

## 9. Estrutura recomendada do repositório

```
california-housing-project/
├── data/
│   └── california_housing.csv 
├── notebooks/
│   └── housing_california.ipynb
├── requirements.txt
└── README.md
```
