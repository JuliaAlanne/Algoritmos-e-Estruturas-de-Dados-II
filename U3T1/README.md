Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

# Análise de Redes com Processamento de Linguagem Natural

Este repositório documenta o trabalho de análise de redes utilizando ferramentas de Processamento de Linguagem Natural (NLP) aplicado aos livros **É Assim Que Acaba** e **É Assim Que Começa** da autora Colleen Hoover.

## Objetivo

Explorar relações linguísticas entre personagens, temas e elementos narrativos dos dois livros mencionados, utilizando técnicas de NLP para extrair informações textuais e representá-las em grafos interativos.

## Tecnologias Utilizadas

- **Python**: Linguagem principal para processamento de texto e análise de dados. 
- **Bibliotecas de NLP**:
  - spaCy
- **Bibliotecas de visualização de grafos**:
  - NetworkX
  - Gephi

## Requisitos do Projeto

### Requisito 1: Seleção e Preparação dos Textos

- Coleta e organização dos textos dos livros **[É Assim Que Acaba](e-assim-que-acaba.txt)** e **[É Assim Que Começa](e-assim-que-comeca.txt)**.
- Limpeza e normalização dos dados textuais para remoção de ruídos.

   foi utilizada a função a seguir para fazer a limpeza dos dados em ambos livros 
/python
def get_data():
    file_path = "/content/e-assim-que-comeca.txt"

    # Ler o conteúdo do arquivo local
    with open(file_path, "r", encoding="utf-8") as file:
      text = file.read()

    # strip header junk
    cutoff = text.index('1. Atlas')
    text = text[cutoff:]

    # strip footer junk
    cutoff = text.rindex("quer ser minha peixinha?")
    text = text[:cutoff]

    # pre-processing to clean the text
    text = text.replace('\r', ' ').replace('\n', ' ')
   # text = text.replace('â\x80\x99', '\'').replace('â\x80\x9c', '"').replace('â\x80\x9d', '""').replace('â\x80\x94', ' ')

    return text

//

### Requisito 2: Análise de PoS Tagging e NER

- Utilização de técnicas de Part-of-Speech Tagging (PoS) para identificar categorias gramaticais.
- Extração de entidades nomeadas (Named Entity Recognition - NER) como personagens, locais e organizações mencionadas nos textos.

### Requisito 3: Geração de Redes

- Construção de grafos com base nas relações entre entidades identificadas.
- Definição de métricas como peso das arestas e conexões relevantes.

### Requisito 4: Análise da Rede

- Cálculo de métricas como grau dos nós, centralidade e agrupamentos.
- Identificação de personagens centrais e comunidades relevantes.

### Requisito 5: Visualização e Produção do Grafo

- Geração de visualizações interativas para exploração dos grafos.
[](img/grafo_acaba.png)
### Requisito 6: Documentação e Divulgação

- Criação de documentação detalhada do projeto, incluindo metodologias e resultados.
- Divulgação do trabalho em plataformas como Medium para compartilhamento de insights.

### Insights Obtidos

- **Personagens centrais**:
  - Relações de proximidade e influência entre os personagens principais.
- **Temas recorrentes**:
  - Principais palavras-chave e suas interdependências nos textos.

[Grafo interativo Livro 1](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network_/#) 
[Grafo interativo Livro 2](https://juliaalanne.github.io/Algoritmos-e-Estruturas-de-Dados-II/U3T1/network/#) 


