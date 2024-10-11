Projeto de Classificação com k-NN

Este projeto realiza a classificação de dados utilizando o algoritmo k-NN (k-Nearest Neighbors). 
O foco é prever se uma pessoa sobreviveu com base em características como classe, gênero, idade, e valor da tarifa.

1. Carregamento e Pré-processamento dos Dados
Utilizamos a biblioteca pandas para carregar e explorar os dados de um arquivo CSV. Durante o pré-processamento, os seguintes passos foram seguidos:
 * Identificação e tratamento de valores ausentes: Colunas numéricas foram preenchidas com a mediana e colunas categóricas com a moda.
 * Conversão de variáveis categóricas: Usamos pd.get_dummies() para converter variáveis categóricas em numéricas, como a coluna Sex, que foi transformada em uma variável binária (Sex_male).

2. Implementação do Algoritmo k-NN
O algoritmo k-NN foi implementado usando a biblioteca scikit-learn. As etapas foram:
 * Divisão dos dados entre treino (70%) e teste (30%) usando train_test_split().
 * Criação de um modelo k-NN com k=3.
 * Treinamento do modelo com os dados de treino.
 * Previsão das classes para o conjunto de teste.

3. Avaliação de Desempenho
Após o treinamento, a avaliação de desempenho foi realizada com base nas seguintes métricas:
 * Acurácia: Mede a proporção de previsões corretas. Utilizamos accuracy_score() para calcular esse valor.
 * Matriz de Confusão: A matriz de confusão foi gerada com confusion_matrix() para analisar as classificações corretas e incorretas em mais detalhes.

4. Observações sobre os Resultados
 * A acurácia foi uma boa métrica inicial para avaliar a performance, mas pode ser insuficiente caso as classes estejam desbalanceadas.
 * A matriz de confusão oferece uma visão detalhada dos erros de classificação, ajudando a identificar se o modelo está tendencioso a favor de uma das classes.
