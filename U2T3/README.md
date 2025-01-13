Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

## Algoritmos Clássicos (Dijkstra e Kruskal)
PARTE 1: Comparando Algoritmos de Dijkstra: Min-Heap e NetworkX

## O que é o Algoritmo de Dijkstra?

O algoritmo de Dijkstra é um método para encontrar o caminho mais curto em grafos ponderados com arestas de pesos positivos. Ele começa de um nó de origem, calcula as menores distâncias para os outros nós e constrói o caminho mais eficiente até o destino.

/////// Dessa forma, na parte 1 desta atividade vamos avaliar o algoritmo de dijkstra compartilhado no arquivo [dijsktra_min_heap](dijsktra_min_heap.ipynb) com a solução presente no networkx e visualizar o resultado no OSMnx.

### Objetivo

O objetivo principal é comparar o desempenho dos dois algoritmos em termos de tempo de execução para diferentes pares de pontos de interesse (POIs) na cidade de Natal-RN, usando:

* Algoritmo de Dijkstra com Min-Heap (implementado manualmente).

* Algoritmo de Dijkstra com NetworkX (função shortest_path).

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

  ### Desenvolvimento

  ..
  
  ### Resultados

Para cada par de origem e destino, foram comparados:

Tempo de Execução:

* O tempo de execução foi medido para os dois algoritmos (Min-Heap e NetworkX), conforme apresentado na figira a baixo.

![](img/comparacao.png)


Visualização de Caminhos:

* Os caminhos gerados pelos algoritmos foram sobrepostos em mapas.

* Azul representa o caminho calculado pelo NetworkX.

* Verde representa o caminho calculado pelo Min-Heap.
  
  ![](img/Grafo_Dijsktra.png)


### Análise:

* Ambos os algoritmos produziram os mesmos caminhos mínimos em termos de rota.

* O algoritmo com NetworkX teve desempenho melhor em tempo de execução.

