Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

# Análise de Redes com Processamento de Linguagem Natural

Este repositório documenta um projeto de análise de redes utilizando ferramentas de Processamento de Linguagem Natural (NLP) aplicado aos livros **É Assim Que Acaba** e **É Assim Que Começa**, da autora Colleen Hoover. O objetivo é explorar o padrão gramatical e semântico do estilo de escrita da autora e entender a evolução das relações entre os personagens ao longo da duologia.

## Objetivo

O objetivo deste projeto é analisar as relações linguísticas entre personagens, temas e outros elementos narrativos nos livros **É Assim Que Acaba** e **É Assim Que Começa**. Através do uso de técnicas de NLP, buscamos explorar a consistência das construções das personagens e examinar como as interações entre elas evoluem ao longo da narrativa.

## Tecnologias Utilizadas

- **Python**: Linguagem principal para o processamento de texto e análise de dados.
- **Bibliotecas de NLP**:
  - **spaCy**: Utilizada para análise linguística, incluindo Part-of-Speech Tagging (PoS) e Named Entity Recognition (NER).
- **Bibliotecas de Visualização de Grafos**:
  - **NetworkX**: Utilizada para construção e análise de redes.
  - **Gephi**: Usada para visualização e análise avançada dos grafos gerados.

## Metodologia

### 1. Seleção e Preparação dos Textos

Foram utilizados os livros **[É Assim Que Acaba](e-assim-que-acaba.txt)** e **[É Assim Que Começa](e-assim-que-comeca.txt)**. A função abaixo foi usada para limpar e normalizar os textos, removendo ruídos como cabeçalhos e rodapés:

```python
def get_data():
    file_path = "/content/e-assim-que-comeca.txt"

    # Ler o conteúdo do arquivo local
    with open(file_path, "r", encoding="utf-8") as file:
        text = file.read()

    # Remover junk do cabeçalho
    cutoff = text.index('1. Atlas')
    text = text[cutoff:]

    # Remover junk do rodapé
    cutoff = text.rindex("quer ser minha peixinha?")
    text = text[:cutoff]

    # Pré-processamento para limpeza do texto
    text = text.replace('\r', ' ').replace('\n', ' ')

    return text
```
### 2. Análise de PoS Tagging e Named Entity Recognition (NER)

- **Part-of-Speech (PoS) Tagging**: Identificação das funções gramaticais das palavras (substantivos, verbos, adjetivos, advérbios, etc.).
- **Named Entity Recognition (NER)**: Identificação e classificação das entidades mencionadas no texto, como personagens, locais e eventos.
  o arquivo [](U3T1.pynb) apresenta a implementação .. 
### 3. Geração de Redes

- Com base nas entidades extraídas, construímos grafos em que as entidades são representadas como nós, e as relações entre elas formam as arestas. Isso permite uma análise visual e quantitativa das interações entre personagens e elementos da narrativa. As figuras a seguir apresenta o grafo dos "é assim que acaba"  e "é assim que começa",respectivamnete.


![](img/grafo_acaba.png)  


![](img/grafo_comeca.png)

### 4. Análise da Rede

- Foram cálculadas de métricas como grau dos nós, centralidade, e hubs.  No qual estas métricas permitem a análise da importância de cada personagem e a estrutura das interações dentro da narrativa. Alem disso, foram foi extraidos a rede de ego ds personagem principal e tambem o k-core da rede. As figuras a seguir apresentam as redes de ego no livro 1 e 2, respectivamnete. 

### 5. Visualização e Produção do Grafo

A visualização dos grafos interativo foi realizada com o uso do **Gephi**, resultando em visualizações interativas que facilitam a exploração das conexões linguísticas e das relações entre os personagens.

![](img/ego1.png)
![](img/ego2.png)
Links para Visualização Interativa dos Grafos

- [Grafo interativo do Livro 1 (É Assim Que Acaba)](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network_/#)  
- [Grafo interativo do Livro 2 (É Assim Que Começa)](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network/#)
  
## Resultados e Insights Obtidos

- **Personagens Centrais**: A análise das redes revelou que a personagem principal apresenta uma construção consistente em ambos os livros, com suas interações e traços de personalidade se mantendo coerentes ao longo da duologia.
  
- **Mudança nas Relações de Personagens**: No livro **É Assim Que Começa**, alguns personagens secundários ganham maior destaque em comparação com **É Assim Que Acaba**, indicando uma evolução nas dinâmicas narrativas. Essa mudança pode ser vista como uma adaptação das relações, refletindo a transição entre os livros da duologia.

- **Estilo de Escrita da Autora**: A autora mantém uma continuidade no estilo de escrita entre os dois livros, ao mesmo tempo em que introduz flexibilidade para o desenvolvimento de novas interações e personagens. A análise mostra como a complexidade do enredo é aprofundada, criando contrastes significativos entre os dois volumes.

## Links para Visualização Interativa dos Grafos

- [Grafo interativo do Livro 1 (É Assim Que Acaba)](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network_/#)  
- [Grafo interativo do Livro 2 (É Assim Que Começa)](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network/#)

## Conclusão

Este estudo demonstrou como ferramentas de NLP podem ser utilizadas para analisar a evolução das relações entre personagens em uma narrativa literária, destacando padrões linguísticos e semânticos que contribuem para a construção das personagens e a progressão do enredo.

