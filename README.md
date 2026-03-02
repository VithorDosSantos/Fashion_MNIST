# Fashion-MNIST Classification com CNN

Projeto de classificação de imagens de roupas usando **Redes Neurais Convolucionais (CNNs)** com **Python + Keras/TensorFlow**.

## Visão geral do projeto

Este notebook apresenta um pipeline completo de visão computacional:
- carregamento dos dados,
- análise inicial,
- pré-processamento,
- treinamento de uma CNN,
- avaliação com acurácia, relatório de classificação e matriz de confusão.

O objetivo é construir um modelo capaz de identificar automaticamente o tipo de peça de roupa a partir de uma imagem em escala de cinza.

## Sobre o dataset (Fashion-MNIST)

Dataset escolhido: https://www.kaggle.com/datasets/zalando-research/fashionmnist?resource=download

### Características principais
- **70.000 imagens** em escala de cinza.
- Resolução de **28x28 pixels**.
- **10 classes** de vestuário.
- Divisão padrão:
	- **Treino:** 60.000 imagens
	- **Teste:** 10.000 imagens

### Classes do problema
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

### Por que esse dataset é interessante?
O Fashion-MNIST é um ótimo dataset introdutório para deep learning em imagens porque:
- é leve e rápido para treinar;
- é mais desafiador que o MNIST de dígitos;
- permite testar CNNs com custo computacional baixo.

## O que é uma CNN (de forma simples)

Uma **CNN (Convolutional Neural Network)** é uma rede neural especializada em imagens.

Ela funciona em etapas:
- **Convolução (`Conv2D`)**: aprende filtros para detectar bordas, texturas e padrões visuais.
- **Pooling (`MaxPooling2D`)**: reduz a dimensionalidade e mantém as características mais importantes.
- **Flatten**: transforma os mapas de características em vetor.
- **Camadas densas (`Dense`)**: realizam a decisão final da classe.

Neste projeto, a CNN aprende automaticamente quais padrões diferenciam cada tipo de roupa.

## Pipeline implementado no notebook

1. Importação de bibliotecas e leitura dos arquivos `.csv`.
2. Conversão para `numpy`, separação entre atributos e rótulos.
3. Normalização dos pixels (escala para [0, 1]).
4. `reshape` para formato esperado pela CNN: `(28, 28, 1)`.
5. Criação e compilação do modelo CNN.
6. Treinamento com validação.
7. Avaliação no conjunto de teste e análise de erros com matriz de confusão.

## Estrutura do repositório

- `Fashion_Mnist.ipynb`: notebook principal com todo o fluxo do projeto.
- `README.md`: documentação do projeto.

> Os arquivos de dados não estão versionados neste repositório para mantê-lo leve e organizado.

## Como executar localmente

1. Baixe o dataset no link do Kaggle.
2. Coloque os arquivos CSV na mesma pasta do notebook.
3. Instale as dependências principais:
	 - `numpy`
	 - `pandas`
	 - `matplotlib`
	 - `seaborn`
	 - `scikit-learn`
	 - `tensorflow` (ou `keras` compatível)
4. Abra o notebook `Fashion_Mnist.ipynb` e execute as células em ordem.

## Interpretação dos resultados

Além da acurácia final, é importante observar:
- **matriz de confusão** para entender quais classes o modelo mais confunde;
- **precision/recall/f1-score** para avaliar desempenho por classe;
- possíveis confusões visuais (por exemplo, peças com formato semelhante).

## Próximos passos sugeridos

- Ajuste de hiperparâmetros (taxa de aprendizado, batch size, número de épocas).
- Inclusão de regularização (`Dropout`, `BatchNormalization`).
- Uso de `EarlyStopping` para evitar overfitting.
- Teste de arquiteturas mais profundas e comparação de resultados.
