# Avaliação da mobilidade no entorno da UFRN, em Natal-RN.

Este trabalho tem como objetivo avaliar a mobilidade no entorno da UFRN, em Natal-RN, utilizando notebooks do [OSMnx](https://github.com/gboeing/osmnx) e a documentação da biblioteca. A análise busca identificar as melhores localizações para a implementação de dock-stations de compartilhamento de bicicletas nas proximidades da universidade, contribuindo para a melhoria da mobilidade e incentivando o uso de meios de transporte sustentável.

Além dos codigo é possivel observar uma breve explicação do projeto no [video]().

* Como forma analisar a rede foi decidido incluir os bairros Lagoa Nova, Candelália, e Capim Macio, no entorno da UFRN, com nós dentro de um raio de 3km de distância.

![](imagens/1.0.png)
### Requisito 1 - Métricas de centralidade
#### Centralidade de graus

![](imagens/2.0.png)

#### Centralidade de Proximidade

![](imagens/3.0.png)

#### Centralidade de Intermediação

![](imagens/4.0.png)
#### Centralidade de Autovetor
![](imagens/5.0.png)

### Requisito 2 - PDF e CDF
![](imagens/6.0.png)
![](imagens/7.0.png)
![](imagens/8.0.png)


### Requisito 3 - Analisando a Matriz de Correlação das Métricas de Centralidade
![](imagens/9.0.png)

### Requisito 4 - Quem é o core/shell da rede?
![](imagens/10.0.png)
