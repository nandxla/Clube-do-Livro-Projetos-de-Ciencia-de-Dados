# Machine Learning - Introdução
Neste primeiro artigo de uma série que está por vir, você terá uma introdução ao Machine Learning. Se você ainda não tem familiaridade com o desenvolvimento de inteligências artificiais, convido você a seguir com a leitura.

A série é baseada no livro **Projetos de Ciência de Dados com Python**, bem como na minha experiência como cientista de dados. Além disso, todos os artigos estarão disponíveis no LinkedIn e no GitHub, juntamente com os códigos desenvolvidos.

# Primeiros Passos
Antes de avançarmos para as análises preditivas, vamos revisar alguns conceitos que considero essenciais. Vale lembrar que é esperado que você já tenha conhecimento de Python, saiba criar funções, usar loops e condicionais, e entenda conceitos básicos como variáveis, entre outros. Nesta seção, irei focar apenas em alguns conceitos fundamentais.

## Listas e *Slices*
Uma lista é uma coleção ordenada de elementos que pode armazenar diferentes tipos de dados.

```python
lista_frutas = ["Maçã", "Pera", "Uva", "Banana"]
lista_numeros_inteiros = list(range(1, 6))

print(lista_numeros_inteiros)

>>> [1, 2, 3, 4, 5]
```

Acima, vimos uma lista de frutas e uma lista de números. Mas onde quero chegar com isso? Uma das manipulações mais importantes na análise de dados, especialmente com dataframes ou matrizes, é o _slice_ (fatiamento), que nos permite selecionar apenas uma parte do nosso conjunto de dados.

```python
print(lista_numeros_inteiros[:3])
>>> [1, 2, 3]

print(lista_numeros_inteiros[-1])
>>> 5
```

Gostaria de destacar duas observações importantes sobre o fatiamento em Python. Primeiro, tanto no _slice_ quanto na função _range_, o primeiro elemento é incluído (faz parte do conjunto), enquanto o último é excluído (não faz parte do conjunto).

Além disso, o _slice_ permite o uso de números negativos: o `-1` representa o último elemento, o `-2` o penúltimo, e assim por diante.

## Anaconda e Gerenciamento de Pacotes
Se você já é programador Python, provavelmente já usou o PIP ou Poetry para gerenciar os pacotes do seu código. Agora, para quem não conhece o Anaconda, ele é um gerenciador de bibliotecas. Ao instalá-lo na sua máquina, ele já traz o Python e todas as bibliotecas essenciais para desenvolvimento em análise e modelagem de dados.

Não vou me aprofundar muito sobre o Anaconda, mas recomendo que visite o site oficial e leia a documentação para entender melhor a ferramenta.

## Conda
Ao instalar o anaconda, abrindo o terminal você terá acesso aos comando do anaconda. Alguns exemplos a seguir:

- `conda list` - Lista todos as bibliotecas instaladas no junto com o ambiente anaconda
- `conda install` - Instala novas libs para que você possa usar


---

# Problemas de um Cientista de Dados
Como Cientista de Dados, grande parte do seu tempo será dedicada à preparação dos dados: carregar _datasets_, tratá-los e examiná-los para garantir que não haja erros. Só depois vem a parte da modelagem preditiva. Mas o que é a modelagem preditiva?

**"É o uso de um modelo matemático ou uma formulação idealizada para aprender os relacionamentos nos dados."**

Vamos explorar cada um desses conceitos e entender as diferenças:

- Um **modelo matemático** é uma representação formal e quantitativa de um fenômeno real, descrevendo a relação entre as variáveis com base nos dados. Um exemplo é o modelo de regressão linear, que cria um espaço multidimensional para cada variável envolvida.
    
- Uma **formulação matemática idealizada** é uma simplificação ou abstração da realidade, capturando a essência do fenômeno sem se preocupar com todas as suas complexidades. Por exemplo, a equação do movimento na física, $F=ma$, ignora o atrito e a resistência do ar, assumindo um ambiente idealizado.
    

Agora, falando de dados tabulares, quando trabalhamos com modelos supervisionados (já vou explicar o que são), temos uma tabela com colunas de características e uma coluna alvo (também chamada de rótulo). O modelo aprende os padrões dos dados e, ao receber novos dados, é capaz de prever o rótulo correspondente.

Existem dois principais tipos de modelos supervisionados:

1. **Modelos de regressão**: Usados para prever rótulos contínuos. Por exemplo, prever o valor de uma casa com base em suas características.
    
2. **Modelos de classificação**: Usados para prever uma variável qualitativa. Um exemplo seria identificar se uma pessoa tem risco de hipertensão com base em fatores como hábitos alimentares e atividade física.
    

Esses são chamados de **modelos supervisionados** porque dependem de um rótulo para aprender os padrões entre as características e o alvo. Além disso, também existem os **modelos não supervisionados**, que trabalham com agrupamentos (clusters). Não vou me aprofundar aqui, mas recomendo que você pesquise mais sobre eles.

---

# Carregando os dados e Jupyter Notebook
Agora, vamos começar carregando nossos dados em um Jupyter Notebook. Mas o que é um Jupyter Notebook? É um ambiente que permite executar seus códigos Python, com uma vantagem significativa em relação a um editor de código padrão: nele, você pode visualizar gráficos, interagir com planilhas e muito mais.

O arquivo que utilizaremos em nossos estudos está localizado em: [Data-Science-Projects-with-Python/Data/default_of_credit_card_clients__courseware_version_1_21_19.xls at master · TrainingByPackt/Data-Science-Projects-with-Python (github.com)](https://github.com/TrainingByPackt/Data-Science-Projects-with-Python/blob/master/Data/default_of_credit_card_clients__courseware_version_1_21_19.xls). Recomendo que você baixe o arquivo, examine-o e tente entender o que cada coluna representa. Além disso, você pode consultar a documentação deste dataset no seguinte link: [Default of Credit Card Clients - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients), onde é explicado o significado de cada coluna.