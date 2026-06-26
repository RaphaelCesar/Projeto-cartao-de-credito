# 💳 Análise de Clientes de Cartão de Crédito & Previsão de Churn

Análise exploratória e modelo preditivo de churn para 2.564 clientes de cartão de crédito utilizando Python, SQL, AWS S3, AWS Athena e Machine Learning.

---

## 📌 Visão Geral do Projeto

Este projeto realiza uma análise completa do comportamento de clientes de cartão de crédito, respondendo 8 perguntas de negócio sobre limites de gastos, padrões de transação, perfil demográfico e engajamento dos clientes.

Um modelo de machine learning para previsão de churn foi desenvolvido e comparado entre 3 algoritmos, identificando clientes de alto risco e quantificando o impacto financeiro do churn potencial.

---

## 🎯 Perguntas de Negócio Respondidas

1. Qual é o perfil demográfico da base de clientes?
2. Quais são os padrões de distribuição de gastos e limites?
3. Quais segmentos de clientes têm maior frequência de transações?
4. Quais fatores estão mais correlacionados com o churn?
5. Qual é o valor financeiro em risco nos segmentos de maior churn?
6. Quais clientes devem ser priorizados em uma campanha de retenção?
7. Como o limite de crédito se relaciona com o engajamento do cliente?
8. Quais variáveis derivadas melhoram a previsão de churn?

---

## 🔍 Principais Resultados

| Métrica | Resultado |
|--------|--------|
| Clientes analisados | 2.564 |
| Melhor AUC-ROC | **0,991** |
| Clientes de alto risco identificados | **203** |
| Precisão no grupo de alto risco | **99%** |
| Receita em risco | **R$ 683.000** |
| Receita preservável com campanha de retenção | **~R$ 205.000** |

> 💡 Uma campanha de retenção direcionada a menos de 10% da base pode preservar aproximadamente R$ 205.000 em receita.

---

## 🧠 Principais Descobertas

- **Frequência de transações** é o principal preditor de churn (maior feature importance)
- Uma variável derivada criada no projeto — **ticket médio** (gasto total / número de transações) — ficou entre as **top 4** features do modelo
- O modelo **XGBoost** superou a Regressão Logística e o Random Forest com AUC-ROC de 0,991

---

## 🛠️ Ferramentas Utilizadas

**Armazenamento e Consulta de Dados**
- AWS S3 — armazenamento de dados brutos e enriquecidos
- AWS Athena — consultas SQL analíticas sobre dados particionados

**Análise e Modelagem**
- Python 3
- Pandas, NumPy — manipulação e limpeza de dados
- Matplotlib, Seaborn — visualização de dados
- Scikit-learn — Regressão Logística, Random Forest
- XGBoost — modelo com melhor desempenho

---

## 📁 Estrutura do Projeto

```
credit-card-analysis/
│
├── notebook.ipynb        # Notebook principal com toda a análise
├── README.md             # Documentação do projeto
└── data/
    └── dataset.csv       # Base de dados (fonte: Kaggle)
```

---

## 🚀 Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/RaphaelCesar/credit-card-analysis.git
```

2. Instale as dependências:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

3. Abra o notebook:
```bash
jupyter notebook notebook.ipynb
```

> **Observação:** AWS S3 e Athena foram utilizados para armazenamento e consulta dos dados no pipeline original. O notebook também pode ser executado localmente utilizando o arquivo CSV na pasta `/data`.

---

## 📊 Dataset

- **Fonte:** [Kaggle — Clientes de Cartão de Crédito](https://www.kaggle.com/code/raphaelcsar/clientes-cart-o-de-cr-dito)
- **Registros:** 2.564 clientes
- **Variáveis:** Dados demográficos, limites de crédito, histórico de transações e métricas de engajamento

---

## 👤 Autor

**Raphael Sousa**
Analista de Dados | Python · SQL · AWS · Power BI

[![LinkedIn](https://img.shields.io/badge/LinkedIn-raphaelsousa08-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/raphaelsousa08)
[![Kaggle](https://img.shields.io/badge/Kaggle-raphaelcsar-20BEFF?style=flat&logo=kaggle)](https://www.kaggle.com/raphaelcsar)
