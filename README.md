# Classificação de Imagens de Satélite

  Projeto de Classificação de Imagens de Satélite RSI-CB256. Esse dataset tem 4 classes distintas obtidas por sensores e imagens do Google Maps. 
  
O projeto foi feito com dois frameworks de Deep Learning:

- Tensorflow/Keras;
- Pytorch.

## Stacks
- Linguagem: Python;
- Bibliotecas: Os, Pathlib, Pandas, Numpy, Matplotlib, Seaborn, PIL, Split-folders, Scikit-learn, Tensorflow, Torch e Torchvision.

## Principais Visualizações do Projeto

### Distribuição das Classes do Dataset
![image](https://user-images.githubusercontent.com/95313119/180498963-edb84636-290a-47ac-89fe-8bb01f3e605b.png)

### Tensorflow

Link: https://github.com/LuanRD/satellite_image_class/blob/main/notebooks/Tensorflow.ipynb

#### Sumário do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499120-5d1f7f8a-d2ae-40e8-910b-e44c0c82f03e.png)

#### Gráficos de Acurácia e Perdas do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499269-f07e00a9-df2d-4cac-ae3c-d88633e8fb11.png)

#### Matriz de Confusão do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499366-dbf5e04e-2e6f-40d8-b7ec-f3bd08650d7e.png)

#### Conclusão

- Os três modelos tiveram o mesmo desempenho no dataset de teste, com 90,01% de acurácia;
- Percebe-se que a complexidade do modelo é diretamente proporcional ao tempo de treinamento;
- Foi o escolhido o primeiro modelo por ser mais simples;
- Maior dificuldade em diferenciar "green_area" e "water", com 50 imagens de "green_area" sendo classificadas erroneamente como "water" e 6 imagens de "water" sendo classificadas como "green_area";
- Esse erro se deu provavelmente devido à semelhança nas cores e características das imagens de ambas as classes.

### Pytorch

Link: https://github.com/LuanRD/satellite_image_class/blob/main/notebooks/Pytorch.ipynb

#### Sumário do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499830-c2720f6b-0428-4e49-aaa3-676b966f656c.png)

#### Gráficos de Acurácia e Perdas do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499878-2e9d04ee-8388-4600-9d39-fe76de3f8107.png)

#### Matriz de Confusão do Melhor Modelo
![image](https://user-images.githubusercontent.com/95313119/180499933-75aa0237-a7e5-4186-873c-a2bba7462734.png)

#### Conclusão

- A rede neural foi treinada usando "CUDA", o que acelerou profundamente o treinamento, ainda mais considerando a complexidade do modelo;
- O modelo performou muito bem em todas as classes, com maior dificuldade em diferenciar entre "cloudy" e "desert", com 11 imagens sendo erroneamente classificadas como "desert";
- O modelo obteve 97,34% de acurácia no dataset de teste, onde obteve 95% de acurácia para "desert" (pior desempenho) e 99,33% de acurácia para "green_area" (melhor desempenho).    

Obrigado pela atenção :D

