# Customer Churn Detection (Detecção de Rotatividade de Clientes)

## Contexto do Projeto

Este projeto aborda o problema de **detecção de Churn** (rotatividade), uma tarefa de classificação binária onde o objetivo é prever quais clientes estão propensos a cancelar seus serviços. A capacidade de prever o churn é de grande valor para as empresas, permitindo que as equipes de retenção atuem de forma proativa.

O desafio central deste projeto foi lidar com um **dataset desbalanceado**, onde o número de clientes que fazem churn é significativamente menor do que o de clientes ativos. A solução envolveu a aplicação de técnicas avançadas de pré-processamento e modelagem.

## Jornada de Desenvolvimento

O projeto foi construído em etapas, demonstrando a evolução de uma solução de Machine Learning:

1.  **Dados Sintéticos**: Inicialmente, utilizamos um dataset sintético para estruturar o problema. Esta fase revelou a importância de métricas como `Precision` e `Recall`, já que a alta `Acurácia` geral se mostrou enganosa.
2.  **Técnicas de Balanceamento**: Após identificar a baixa performance na classe minoritária (`Churn`), aplicamos a técnica **SMOTE** (Synthetic Minority Over-sampling Technique) para balancear os dados de treino, melhorando a capacidade do modelo de detectar clientes em risco.
3.  **Modelagem Avançada**: Trocamos o modelo inicial **Random Forest** por um mais potente, o **XGBoost**, que demonstrou maior capacidade de aprender os padrões em dados complexos e desbalanceados.
4.  **Dados Reais**: Por fim, migramos para um dataset de telecomunicações real do Kaggle, o que levou a um salto significativo no desempenho, validando a importância de ter dados de alta qualidade para o treinamento do modelo.

## Interpretação dos Resultados Finais

O modelo final foi avaliado com as seguintes métricas, que são essenciais para um problema de detecção de churn:

* **Precision (Churn): 0.58**
    > **Interpretação:** Das vezes que o modelo previu que um cliente faria churn, ele estava correto em **58%** das vezes.
* **Recall (Churn): 0.59**
    > **Interpretação:** De todos os clientes que realmente fizeram churn, o modelo conseguiu identificar **59%** deles.
* **F1-Score (Churn): 0.58**
    > **Interpretação:** O F1-Score, que equilibra as duas métricas anteriores, indica uma boa performance geral para a classe de interesse.
* **Acurácia Geral: 0.78**
    > **Interpretação:** O modelo acertou 78% das previsões no total. Este número é mais baixo do que no início, mas é um reflexo honesto do desempenho em um cenário desbalanceado.

A **Matriz de Confusão** do resultado final mostra visualmente os acertos e erros do modelo, confirmando que a maioria dos erros de previsão são classificados como falsos positivos (o modelo prevê churn, mas o cliente não sai) e não como falsos negativos (o cliente sai, mas o modelo não o detecta), o que é preferível para uma equipe de retenção.

## Como Executar o Projeto

O código-fonte está disponível no notebook `customer_churn_detection.ipynb`.

1.  **Baixe o Dataset**: O projeto utiliza o dataset [Telco Customer Churn do Kaggle](datasets/WA_Fn-UseC_-Telco-Customer-Churn.csv). Faça o download do arquivo CSV.
2.  **Abra no Colab**: Faça o upload do arquivo CSV para o Google Colab e execute o notebook `customer_churn_detection.ipynb` passo a passo.
3.  **Dependências**: Certifique-se de que as bibliotecas `imblearn` e `xgboost` estejam instaladas.