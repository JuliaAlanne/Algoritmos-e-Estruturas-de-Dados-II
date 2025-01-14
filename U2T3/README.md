Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

## Algoritmos Clássicos (Dijkstra e Kruskal)

#### Algoritmo de Dijkstra:

O algoritmo de Dijkstra é um método para encontrar o caminho mais curto em grafos ponderados com arestas de pesos positivos. Ele começa de um nó de origem, calcula as menores distâncias para os outros nós e constrói o caminho mais eficiente até o destino.

#### Algoritmo de Kruskal

O algoritmo de Kruskal é um método eficiente e amplamente utilizado para determinar a Árvore Geradora Mínima (Minimum Spanning Tree - MST) em um grafo ponderado e conectado, garantindo a menor soma possível dos pesos das arestas que conectam todos os vértices.


## PARTE 1: Comparando Algoritmos de Dijkstra: Min-Heap e NetworkX 

### Objetivo
O objetivo principal é  avaliar o  desempenho  do algoritmo de dijkstra compartilhado no arquivo [dijsktra_min_heap](dijsktra_min_heap.ipynb) com a solução presente no networkx (função shortest_path)  para diferentes pares de pontos de interesse (POIs) na cidade de Natal-RN e visualizar o resultado no OSMnx.


### Desenvolvimento
Foram definidos os seguintes POIs (Origens, Destino):

  * Shopping Midway Mall, UFRN
  * Universidade Federal do Rio Grande do Norte (UFRN), Morro do careca
  * Praia de Ponta Negra, Praia do Meio
  * Arena das Dunas, Centro Histórico de Natal
  * Parque das Dunas,  Parnamirim (Av. Ayrton Senna)
  * Centro Histórico de Natal, Praia de Ponta Negra
  * Praia do Forte, Shopping Via Direta
  * Shopping Natal Sul,Parque das Dunas
  * Rodoviária de Natal, Arena das Dunas
  * Aeroporto Internacional de Natal (São Gonçalo do Amarante), Shopping Partage Norte
  
### Resultados

Para cada par de origem e destino, foram comparados:

Tempo de Execução:

* O tempo de execução foi medido para os dois algoritmos (Min-Heap e NetworkX), conforme apresentado na figura a baixo.

![](img/comparacao.png)


Visualização de Caminhos:

* Os caminhos gerados pelos algoritmos foram sobrepostos em mapas.

  
  ![](img/Grafo_Dijsktra.png)


### Análise:

* Ambos os algoritmos produziram os mesmos caminhos mínimos em termos de rota.

* O algoritmo com NetworkX teve desempenho melhor em tempo de execução.

## PARTE 2 - Kruskal

### Objetivo

### Desenvolvimento

### Resultados
  ![](img/kruskal.png)


