Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

# Análise da Rede do Bairro Lagoa Nova - Natal/RN usando a biblioteca OSMnx 

Este projeto tem como objetivo explorar as funcionalidades da biblioteca OSMnx para realizar uma análise detalhada da rede viária do bairro Lagoa Nova, em Natal/RN. Utilizando diversas métricas de análise de rede, buscaremos responder a perguntas relevantes sobre a estrutura e o funcionamento da infraestrutura viária local. Foi gravado um [Video](https://www.loom.com/share/cf37742cd4f64a63bd2b00adac178eba?sid=36504562-474d-4b85-861c-7173791b537d) explicativo do desenvolvimento da atividade.

![Descrição da imagem](imagens/01..png)

No mapa gerado pelo OSMnx, os nós e arestas são elementos essenciais da estrutura da rede viária:

* Nós: Os nós representam pontos de interseção, cruzamentos ou locais onde as ruas começam ou terminam, como acessos e ramificações.

* Arestas: As arestas correspondem às ruas ou segmentos de rua que ligam dois nós, representando os trechos percorríveis da via entre interseções ou outros pontos importantes na rede.
* ![Descrição da imagem](imagens/02..png)

### Quantos componentes conectados existem na rede viária de Lagoa Nova e qual é o tamanho do maior componente conectado ?
Componentes conectados = 33
Maior componente conectado = 1155

A rede viária de Lagoa Nova possui 33 componentes conectados, indicando que está fragmentada em várias sub-redes independentes, o que limita a conectividade e dificulta a mobilidade, especialmente em situações de congestionamento. 

O maior componente, com 1155 nós, representa a parte mais interconectada e acessível, abrangendo as principais vias e facilitando o deslocamento e o acesso a serviços. A presença de áreas isoladas sugere a necessidade de intervenções para melhorar a integração entre essas sub-redes, promovendo uma rede mais acessível e eficiente para os moradores. 
O grafico a seguir apresenta o maior componente conectado, ou seja, a maior sub-rede.

### Qual é o coeficiente de agrupamento médio da rede de Lagoa Nova?
 coeficiente de agrupamento médio = 0,0254
 
 O coeficiente de agrupamento médio de 0,0254 revela uma conectividade muito baixa entre as interseções da rede viária de Lagoa Nova, indicando poucas alternativas de rotas locais. Esse valor sugere uma dependência das vias principais, o que pode aumentar o congestionamento nessas áreas. Uma alternativa para melhorar a mobilidade é criar mais conexões entre ruas próximas poderia elevar o coeficiente de agrupamento, promovendo uma rede mais integrada, com rotas alternativas que diminuem a pressão sobre as vias principais e facilitam o deslocamento pelo bairro.
 ### Qual o caminho mais curto para ir do Departamento de Engenharia de Computação e Automação (DCA) ao Arena das Dunas?

Para encontrar o caminho mais curto do DCA até o Arena das Dunas,utilizaremos a biblioteca OSMnx e NetworkX para calcular a rota entre os dois pontos.
O grafico a seguir apresenta a rota do caminho mais curto para dir do DCA/UFRN ao Arena das Dunas.
![Grafico do maior componente conectado](imagens/03..png)

