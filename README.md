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
---

## Como Rodar os Projetos

Cada projeto foi desenvolvido no Google Colab. Você pode clicar no link de cada projeto e abrir diretamente no Colab para explorar e executar o código.
Para rodar localmente, você precisará instalar as dependências listadas em cada notebook.