Claro\! Aqui está um README simples e direto para este projeto, escrito em português para corresponder ao conteúdo do notebook.

-----

# Análise Preditiva de Churn de Clientes de Telecomunicações

## 📝 Visão Geral do Projeto

Este projeto utiliza técnicas de Data Science para analisar dados de clientes de uma empresa de telecomunicações (fictícia), com o objetivo de prever a evasão de clientes (Churn). O notebook abrange desde a extração e tratamento dos dados até a construção, avaliação e interpretação de modelos de machine learning.

## 🎯 Objetivo

O objetivo principal é construir um modelo preditivo capaz de identificar clientes com alta probabilidade de cancelar seus serviços. Além disso, o projeto busca identificar quais fatores (variáveis) mais influenciam a decisão de um cliente em evadir, gerando insights para estratégias de retenção.

## 📊 Dataset

O conjunto de dados utilizado é o `TelecomX_Data.json`, que contém informações sobre o perfil dos clientes, os serviços contratados e dados financeiros da conta.

## 🛠️ Metodologia

O projeto foi estruturado nas seguintes etapas:

1.  **Extração:** Os dados foram carregados a partir de uma URL pública em formato JSON.
2.  **Transformação e Limpeza:**
      * Tratamento de valores ausentes e conversão de tipos de dados.
      * Criação de uma nova feature (`contas_diarias`) para enriquecer a análise.
      * Transformação de colunas categóricas em formato numérico (One-Hot Encoding) para serem utilizadas pelos modelos.
3.  **Análise Exploratória e Correlação:**
      * Análise da correlação entre as variáveis e a variável alvo (Churn).
      * Visualização da distribuição de dados importantes, como o tempo de contrato (`customer.tenure`) e os gastos totais (`account.Charges.Total`), em relação à evasão.
4.  **Modelagem Preditiva:**
      * Os dados foram divididos em conjuntos de treino (70%) e teste (30%).
      * Dois modelos de classificação foram treinados: **Random Forest** e **Árvore de Decisão**.
5.  **Avaliação dos Modelos:**
      * Os modelos foram avaliados com base em métricas como Acurácia, Precisão, Recall, F1-Score e a Matriz de Confusão.

## 🚀 Principais Resultados e Insights

  * **Desempenho dos Modelos:** O modelo **Random Forest** apresentou um desempenho geral superior, com uma acurácia de **78%** e um F1-Score de **53%**, superando a Árvore de Decisão.
  * **Fatores de Churn:** As variáveis mais importantes para prever a evasão de clientes foram:
    1.  **Gastos do Cliente:** `contas_diarias`, `account.Charges.Monthly` e `account.Charges.Total`.
    2.  **Tipo de Contrato:** Clientes com contratos do tipo `Mês a Mês` são muito mais propensos a evadir.
    3.  **Tempo de Contrato (`tenure`):** Clientes com menor tempo de contrato tendem a cancelar mais.

## ⚙️ Como Executar

1.  Certifique-se de ter um ambiente Python (como Jupyter Notebook ou Google Colab) configurado.
2.  Instale as bibliotecas necessárias:
    ```bash
    pip install pandas matplotlib seaborn scikit-learn requests numpy
    ```
3.  Abra o arquivo `challange_3.ipynb` e execute as células em ordem sequencial.

## 💻 Tecnologias Utilizadas

  * **Python 3**
  * **Pandas:** para manipulação e análise de dados.
  * **Scikit-learn:** para a construção e avaliação dos modelos de machine learning.
  * **Matplotlib & Seaborn:** para visualização de dados.
  * **Requests:** para extração dos dados via web.
  * **NumPy:** para operações numéricas.
