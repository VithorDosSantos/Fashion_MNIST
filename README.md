# Fashion-MNIST Classification (CNN)

Projeto de classificação de imagens de roupas usando **Rede Neural Convolucional (CNN)** com Python/Keras.

## Dataset

Este projeto usa o **Fashion-MNIST**:
- Fonte: https://www.kaggle.com/datasets/zalando-research/fashionmnist?resource=download
- 70.000 imagens em escala de cinza (28x28)
- 10 classes de vestuário

Classes:
1. T-shirt/top  
2. Trouser  
3. Pullover  
4. Dress  
5. Coat  
6. Sandal  
7. Shirt  
8. Sneaker  
9. Bag  
10. Ankle boot

## Estrutura deste repositório

- `Fashion_Mnist.ipynb`: notebook principal com todo o fluxo (carregamento, pré-processamento, treino e avaliação).
- `README.md`: descrição do projeto.

> Os arquivos de dados não estão versionados neste repositório para manter o projeto leve e organizado.

## Como executar

1. Baixe o dataset no link do Kaggle acima.
2. Coloque os arquivos CSV na mesma pasta do notebook.
3. Abra o notebook `Fashion_Mnist.ipynb`.
4. Execute as células em ordem.

## Objetivo do notebook

- Carregar e explorar o dataset Fashion-MNIST.
- Preparar os dados para entrada em CNN.
- Treinar um modelo de classificação multiclasse.
- Avaliar desempenho com métricas e matriz de confusão.
