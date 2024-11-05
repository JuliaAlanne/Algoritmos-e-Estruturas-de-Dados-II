# Avaliação da mobilidade no entorno da UFRN, em Natal-RN.
## Descrição
Este trabalho tem como objetivo avaliar a mobilidade no entorno da UFRN, em Natal-RN, utilizando notebooks do [OSMnx](https://github.com/gboeing/osmnx) e a documentação da biblioteca. A análise busca identificar as melhores localizações para a implementação de dock-stations de compartilhamento de bicicletas nas proximidades da universidade, contribuindo para a melhoria da mobilidade e incentivando o uso de meios de transporte sustentável.

Além dos codigo é possivel observar uma breve explicação do projeto no [video]().

* Como forma analisar a rede foi decidido incluir os bairros Lagoa Nova, Candelália, e Capim Macio, no entorno da UFRN, com nós dentro de um raio de 3km de distância.

![](imagens/1.0.png)
### Requisito 1 - Métricas de centralidade
#### Centralidade de graus

![](imagens/2.0.png)

Na rede acima os nós em tons mais claros (amarelos)apresentam uma centralidade de proximidade mais alta, o que significa que são interseções com acessibilidade vantajosa, possivelmente no centro do bairro ou em pontos de convergência de várias ruas. Esses nós estão em uma posição central dentro da rede e podem ser alcançados mais rapidamente a partir de qualquer outro nó. Diferente dos nós em tons mais escuros (azul e roxo), ou seja, estes nós têm centralidade de proximidade mais baixa, o que indica que estão em regiões menos conectadas. Eles provavelmente precisam de mais etapas (ou ruas) para acessar a maioria dos outros pontos da rede.
#### Centralidade de Proximidade

![](imagens/3.0.png)

#### Centralidade de Intermediação

![](imagens/4.0.png)
#### Centralidade de Autovetor
![](imagens/5.0.png)

### Requisito 2 - PDF e CDF
Análise da CDF e PDF dos graus dos nós para compreender o comportamento da rede (se ela segue uma distribuição de tipo "lei de potência", que é comum em redes complexas). 

Análise multivariada das métricas de centralidade:
Aplicação de técnicas de análise multivariada para observar como diferentes métricas de centralidade estão relacionadas e como elas podem ser usadas para identificar zonas de alta mobilidade.
![](imagens/6.0.png)
![](imagens/7.0.png)
![](imagens/8.0.png)

A partir das métricas de centralidade e da análise multivariada, sugerir os bairros ou interseções de alta centralidade como locais ideais para a instalação de dock-stations de bicicletas.

### Requisito 3 - Analisando a Matriz de Correlação das Métricas de Centralidade
![](imagens/9.0.png)

### Requisito 4 - Quem é o core/shell da rede?
![](imagens/10.0.png)
