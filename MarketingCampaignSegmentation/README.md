# Marketing Campaign Segmentation (Segmentação de Campanhas de Marketing)

## Contexto do Projeto

Este projeto demonstra a aplicação de técnicas de **aprendizado não supervisionado** para segmentar clientes de um e-commerce em grupos com base em seu comportamento de consumo. A segmentação é uma ferramenta poderosa para o marketing, pois permite a criação de campanhas direcionadas e personalizadas para cada perfil de cliente.

O objetivo principal foi utilizar o algoritmo de agrupamento **K-Means** em um dataset real para identificar padrões de compra e, a partir daí, definir perfis de clientes que podem ser o alvo de estratégias de marketing específicas.

## Jornada de Desenvolvimento

O projeto focou na preparação e análise de dados para um modelo de agrupamento, utilizando os seguintes componentes:

* **Pré-processamento de Dados:**
    * **Seleção de Características**: Foram utilizadas as colunas de `Renda Anual` e `Pontuação de Gastos` como base para a segmentação, pois são as características mais relevantes para a análise de perfil de consumo.
    * **Normalização de Dados**: Como o K-Means é sensível à escala, os dados foram normalizados usando o `StandardScaler` para garantir que ambas as características tivessem a mesma importância na criação dos clusters.
* **Agrupamento e Modelagem:**
    * **Método do Cotovelo**: O **Método do Cotovelo (Elbow Method)** foi aplicado para determinar o número ideal de clusters (`k`) antes de treinar o modelo.
    * **K-Means**: O algoritmo **K-Means** foi treinado com o número ideal de clusters para agrupar os clientes em perfis distintos.
* **Avaliação de Resultados:**
    * A avaliação do modelo de agrupamento foi feita de forma visual, através de um gráfico de dispersão que mostra a segmentação dos clientes.
    * A interpretação dos clusters foi realizada a partir da análise dos centros de cada grupo, permitindo a definição de perfis como "Clientes VIPs" e "Compradores Esporádicos".

## Interpretação dos Resultados Finais

O modelo identificou 5 perfis de clientes distintos, revelados pelo gráfico de dispersão. Cada cluster representa um perfil com um comportamento de compra específico, que pode ser a base para diferentes estratégias de marketing:

* **Cluster 0 (Roxo - Centro)**: Clientes com renda e pontuação de gastos medianas.
* **Cluster 1 (Azul Escuro - Canto Inferior Esquerdo)**: Clientes com baixa renda e baixo gasto.
* **Cluster 2 (Verde - Canto Superior Esquerdo)**: Clientes de baixa renda, mas com alto gasto.
* **Cluster 3 (Ciano - Canto Superior Direito)**: Clientes de alta renda e alto gasto ("Clientes VIPs").
* **Cluster 4 (Amarelo - Canto Inferior Direito)**: Clientes de alta renda, mas com baixo gasto.

## Como Executar o Projeto

O código-fonte está disponível no notebook `customer_segmentation.ipynb`.

1.  **Baixe o Dataset**: O projeto utiliza o dataset [Mall Customer Segmentation do Kaggle](datasets/Mall_Customers.csv). Faça o download do arquivo CSV.
2.  **Abra no Colab**: Faça o upload do arquivo CSV para o Google Colab e execute o notebook `MarketingCampaignSegmentation.ipynb` passo a passo.
3.  **Dependências**: As principais bibliotecas utilizadas já vêm pré-instaladas no ambiente do Colab.