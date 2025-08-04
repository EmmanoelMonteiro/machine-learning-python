# Classificação de Emoções a partir de Texto

## Contexto do Projeto

Este projeto demonstra a aplicação de um modelo de Machine Learning para a tarefa de **Classificação de Emoções a partir de Texto**. O objetivo é criar um algoritmo capaz de identificar e categorizar a emoção expressa em uma frase ou texto curto (por exemplo: alegria, tristeza, medo) com base em seu conteúdo.

Para isso, utilizamos um dataset público de textos rotulados com seis emoções distintas, empregando técnicas de processamento de linguagem natural e um modelo clássico de classificação.

## Fluxo do Projeto

O projeto seguiu as seguintes etapas principais:

1.  **Carregamento dos Dados**: Utilizamos a biblioteca `datasets` do Hugging Face para importar um dataset de emoções já pré-processado e dividido em conjuntos de treino e teste.
2.  **Pré-processamento e Vetorização do Texto**: Textos não podem ser processados diretamente por modelos numéricos. Por isso, usamos o **TF-IDF (Term Frequency-Inverse Document Frequency)** para converter cada frase em um vetor de números, onde a importância de cada palavra é considerada.
3.  **Treinamento do Modelo**: Um modelo de **Random Forest Classifier** foi treinado com os dados vetorizados para aprender os padrões que diferenciam cada emoção.
4.  **Avaliação de Desempenho**: O modelo treinado foi avaliado com os dados de teste para medir sua eficácia. As métricas de avaliação incluem acurácia e um relatório detalhado de classificação, além da visualização da **matriz de confusão**.

## Interpretação dos Resultados

A avaliação do modelo nos permite entender sua performance. Diferentemente de problemas mais simples, como a classificação das flores Íris, a classificação de texto é um desafio complexo.

* **Acurácia**: Indica a porcentagem total de previsões corretas do modelo. Uma acurácia de, por exemplo, 70% significa que o modelo acertou 7 de cada 10 textos no conjunto de teste.
* **Precision, Recall e F1-Score**: Essas métricas detalham a performance para cada emoção.
    * **Precision**: Responde: "Das vezes que o modelo previu 'alegria', em quantas ele acertou?"
    * **Recall**: Responde: "De todos os textos que eram realmente 'alegria', quantos o modelo conseguiu encontrar?"
    * **F1-Score**: Fornece um equilíbrio entre `precision` e `recall`, sendo uma ótima métrica para ter uma visão geral da performance de cada classe.
* **Matriz de Confusão**: É a ferramenta mais poderosa para entender os erros do modelo.
    * A diagonal principal (do canto superior esquerdo para o inferior direito) mostra o número de **acertos** para cada emoção.
    * As células fora da diagonal mostram as **confusões**; por exemplo, se a célula da linha 'tristeza' e coluna 'medo' tiver um valor alto, isso indica que o modelo está frequentemente confundindo textos tristes com textos de medo.

## Como Rodar o Código

O código-fonte para este projeto está disponível no notebook `classificacao_emocoes.ipynb`.

1.  **Abra o Notebook:** Clique no arquivo `.ipynb` e, em seguida, clique no botão "Open in Colab" para executá-lo diretamente no Google Colab.
2.  **Execute as Células:** Basta seguir as células do notebook sequencialmente. O ambiente do Colab já inclui a maioria das bibliotecas necessárias, e as dependências adicionais são instaladas na primeira célula.