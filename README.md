# Recomendação de Músicas

## O projeto
Este projeto, feito em grupo para disciplina de Aprendizagem de Máquina, teve como objetivo implementar técnicas de recomendação de músicas. As técnicas utilizadas foram:
1. Ordenação por popularidade
2. Similaridade entre músicas (Content-based filtering)

## Os datasets
Os datasets utilizados foram:
1. Spotify Million Playlist Dataset Challenge (Conjunto de até 1 milhão de playlists)
2. API do Spotify (Conjunto de mais de 2 milhões de tracks)

Foi realizado um estudo com os atributos das faixas fornecidas pela API do Spotify e esses foram filtrados e modificado de forma que se mantivessem apenas aqueles que condizessem com a natureza contínua que permitisse o cálculo da distância euclidiana.

## Ordenação por popularidade
Como já era de se esperar, o método de ordenação de popularidade não é customizável e se baseia apenas na pontuação de popularidade fornecida nos metadados das tracks do Spotify.

![1](https://user-images.githubusercontent.com/20979520/189246406-97172cf7-bd72-4b0b-b579-dc6a9de7e2a0.png)

## Content-based filtering
A entrada desse modelo pode ser uma track única, ou uma playlist, em que a média de seus atributos foram calculadas. Então são calculadadas as distâncias euclidianas entre a entrada e as músicas do dataset. O resultado consiste nas k músicas com as menores distâncias com relação a entrada. Nos exemplos abaixo, feitos para alguns gêneros musicais, a primeira faixa consiste na música de entrada.

### Música clássica
![2](https://user-images.githubusercontent.com/20979520/189247297-840d7875-abf1-4406-8b7f-2af0e4fe6360.png)

### Música eletrônica
![3](https://user-images.githubusercontent.com/20979520/189247300-31cb9fea-c869-4cd2-a7df-91d0f2fa5b00.png)

### Música de anime
![4](https://user-images.githubusercontent.com/20979520/189247301-325986c9-1931-476f-9483-59cc2330bd24.png)

### Música rap
![5](https://user-images.githubusercontent.com/20979520/189248704-7c155934-1c11-4cbc-8ee1-94b131925758.png)

## Resultados

### Ordenação por popularidade
Em geral, os resultados apresentados pelo primeiro modelo, mais genérico, são insatisfatórios pois as músicas mais populares podem não correspondem ao gosto de muitas pessoas. Além disso, não há personalização no mesmo de acordo com o usuário.

### Content-based filtering
Para alguns gêneros, como clássica, eletrônica e anime, os resultados pareceram bastante satisfatórios, no entando alguns gêneros como rap tiveram resultados que deixaram a desejar. Quando a entrada é uma playlist, o resultado passa a ser ainda mais inconsistente, principalmente quando as músicas dessa não são muito semelhantes.

## Referências
Recommender Systems: Machine Learning Metrics and Business Metrics. Neptune. 
Disponível em: <https://neptune.ai/blog/recommender-systems-metrics>

Spotify Million Playlist Dataset Challenge. Trabalhos ABNT. 
Disponível em: <https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge>
