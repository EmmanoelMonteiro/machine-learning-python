# Portfólio de Projetos de Machine Learning com Python

Olá! Bem-vindo(a) ao meu portfólio de projetos de Machine Learning. Aqui, você encontrará uma coleção de soluções práticas para cenários diversos, utilizando Python e bibliotecas como Scikit-Learn, Pandas e Matplotlib.

Cada projeto é uma jornada de aprendizado, cobrindo o fluxo completo de um problema de ML:

* Carregamento e Pré-processamento de Dados
* Divisão em Treino e Teste
* Treinamento e Avaliação de Modelos
* Análise de Métricas e Interpretação de Resultados

---

## Projetos

### 1. Classificação de Emoções a partir de Texto
* **Cenário:** Criar um modelo que classifica textos em diferentes emoções (alegria, tristeza, etc.).
* **Modelo:** Random Forest Classifier
* **Técnicas:** Vetorização de texto com TF-IDF.
* **Resultados:** O modelo alcançou uma acurácia de ~70%, e a matriz de confusão revelou insights sobre quais emoções são mais frequentemente confundidas.
* **Link para o Projeto:** [Classificação de Emoções a partir de Texto](ClassifyingEmotionsText/README.md)

### 2. Detecção de Churn em Clientes de Telecom
* **Cenário:** Prever quais clientes de uma empresa de telecomunicações têm maior probabilidade de cancelar seus serviços (churn). O desafio principal foi o **desbalanceamento de classes**.
* **Modelo:** XGBoost Classifier
* **Técnicas:** Pré-processamento de dados reais, One-Hot Encoding e balanceamento de classes com SMOTE.
* **Resultados:** O modelo alcançou um `recall` de 59% e uma `precision` de 58% na classe de `Churn`, mostrando um desempenho robusto em um cenário de dados desbalanceados.
* **Link para o Projeto:** [Acessar Customer Churn Detection](CustomerChurnDetection/README.md)

### 3. Agrupamento de Clientes de um E-commerce
* **Cenário:** Segmentar clientes em diferentes grupos de comportamento de consumo com base em sua renda e gastos para criar campanhas de marketing direcionadas.
* **Modelo:** K-Means Clustering
* **Técnicas:** Método do Cotovelo (Elbow Method) para determinar o número ideal de clusters e `StandardScaler` para normalização dos dados.
* **Resultados:** O modelo identificou 5 perfis distintos de clientes, variando de "Clientes VIPs" (alta renda, alto gasto) a "Compradores Econômicos" (alta renda, baixo gasto).
* **Link para o Projeto:** [Acessar o Marketing Campaign Segmentation](MarketingCampaignSegmentation/README.md)

---

## Como Rodar os Projetos

Cada projeto foi desenvolvido no ambiente do Google Colab para garantir a reprodutibilidade. Para executá-los, siga os passos abaixo:

1.  **Baixe os Arquivos**: Faça o download do arquivo `.ipynb` do projeto desejado e de seu respectivo arquivo de dados (`.csv`).
2.  **Abra o Colab**: Vá para o Google Colab e faça o upload do notebook (`.ipynb`).
3.  **Faça o Upload dos Dados**: Dentro do ambiente do Colab, faça o upload do arquivo de dados (`.csv`) para a pasta de arquivos da sua sessão.
4.  **Execute as Células**: Execute as células do notebook sequencialmente. O ambiente do Colab já inclui a maioria das bibliotecas necessárias.

Alternativamente, você pode clonar o repositório completo para sua máquina local e rodar os notebooks usando um ambiente Python, como o Jupyter Notebook.