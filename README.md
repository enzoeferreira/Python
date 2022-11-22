- [Estudos em Python](#estudos-em-python)
  - [Udemy](#udemy)
  - [Google Style Guide](#google-style-guide)
- [Syntax](#syntax)
  - [Comentários](#comentários)
  - [Comandos de repetição](#comandos-de-repetição)
  - [Tipos de dados](#tipos-de-dados)
  - [Operadores](#operadores)
  - [Atribuição de variável](#atribuição-de-variável)
- [Funções](#funções)
  - [Criação de funções](#criação-de-funções)
  - [print()](#print)
  - [input()](#input)
  - [range()](#range)
  - [len()](#len)
  - [round()](#round)
  - [min()/max()](#minmax)
  - [sum()](#sum)
  - [type()](#type)
  - [exit()](#exit)
- [Listas, Tuplas, Sets e Dicionários](#listas-tuplas-sets-e-dicionários)
  - [Listas (list)](#listas-list)
    - [Criação de listas](#criação-de-listas)
    - [Operações com listas](#operações-com-listas)
    - [Print de listas](#print-de-listas)
    - [Acessar elementos](#acessar-elementos)
    - [Alterar elementos](#alterar-elementos)
    - [Verificação de elementos](#verificação-de-elementos)
    - [Intervalo de listas (Slice)](#intervalo-de-listas-slice)
    - [Tamanho de listas len()](#tamanho-de-listas-len)
    - [Soma de listas](#soma-de-listas)
    - [Map](#map)
  - [Tuplas (tuple)](#tuplas-tuple)
  - [Sets](#sets)
    - [Operações matemáticas](#operações-matemáticas)
  - [Dicionários (dict)](#dicionários-dict)
- [Métodos](#métodos)
  - [Class String](#class-string)
    - [Operações com strings](#operações-com-strings)
    - [Verificação de ocorrência](#verificação-de-ocorrência)
    - [Acessar elementos](#acessar-elementos-1)
    - [Formatação](#formatação)
  - [Class List](#class-list)
    - [Adicionar elementos](#adicionar-elementos)
    - [Remover elementos](#remover-elementos)
    - [Verificiar ocorrência](#verificiar-ocorrência)
    - [Contagem de ocorrência](#contagem-de-ocorrência)
    - [Ordenação de listas](#ordenação-de-listas)
    - [Cópia de listas](#cópia-de-listas)
    - [Join](#join)
  - [Class Set](#class-set)
    - [Adicionar/Remover elementos](#adicionarremover-elementos)
- [Inclusão de bibliotecas](#inclusão-de-bibliotecas)
- [Funções importantes](#funções-importantes)

# Estudos em Python
## [Udemy](https://www.udemy.com/course/curso-algoritmos-logica-de-programacao/)
## [Google Style Guide](https://github.com/google/styleguide/blob/gh-pages/pyguide.md)

# Syntax

## Comentários
```py
# Comentários na linha utilizam "#"

"""
Comentários em várias linhas
utilizam no início e fim 3 aspas seguidas
""" 
```

## Comandos de repetição
```py
if condição:
    # comando (PRECISA DE IDENTAÇÃO)
elif: # Equivalente ao else if
    # comando (PRECISA DE IDENTAÇÃO)
else:
    # comando (PRECISA DE IDENTAÇÃO)
# Na condição, qualquer expressão que tenha um valor != 0 é considerada True

a if condição else b
# Condição TRUE  -> Executa A
# Condição FALSE -> Executa B

try:
    # comando
except:
    # comando, caso o comando acima der erro

while condição:
    # comando

for variavel in sequencia:
    # comando
"""
Sequência é qualquer tipo sequencial do python
Ex: Lista, String, Tupla etc.
"""
```

## Tipos de dados

```py
int -> 11 # Inteiro
float -> 11.10 # Float (Números decimais)
str -> "Enzo" # String (Texto)
bool -> True # Booleana (True ou False)
None # NoneType (Nada, vazio, algo a ser preenchido etc.)
```
Casting
```py
a = "1"
b = "1"
resultado = int(a) + int(b) # resultado = 2 ao invés de "11"

# Com bool(), qualquer número != 0 e qualquer string != "" resultam em True
```

## Operadores

    +  -> Adição
    -  -> Subtração
    *  -> Multiplicação
    /  -> Divisão
    // -> Divisão Inteira
    %  -> Resto da divisão
    ** -> Potenciação

    >  -> Maior
    <  -> Menor
    >= -> Maior ou igual
    <= -> Menor ou igual
    == -> Igual
    != -> Diferente

    and -> e
    or  -> ou
    not -> não

    += -> Incrementa
    -= -> Decréscimo
    Outros operadores também podem ser combinados com "="

## Atribuição de variável

```py
x = 10 # Atribui 10 a "x"
x, y = 10, 20 # Atribui 10 a "x" e 20 a "y"

# Obs: Python é case sensitive, ou seja, Var != aar
```

# Funções

## Criação de funções
```py
def nome(args): # Define a função "nome" que requer "input"
    return var # Retorna a variável "var"

def nome(arg:type): # Definição de função com type hint do argumento
def nome(arg:typeIn)->typeOut: # Define a função com type hint de input e output

def nome(arg = defaultValue): # Define a função com valor padrão p/ argumento
def nome(arg:type = defaultValue): # Define a função com type hint e valor padrão
"""
Type Hint não tem muito uso prático, apenas no autocompletar
em algumas IDEs, é tipo um comentário
"""
```

## print()
```py
print(var) # Printa uma variável
print("Hello, World!") # Printa um texto
print(sep = " ", end = "\n")
"""
Por padrão:
sep = " "  -> Separador entre argumentos é o espaço
end = "\n" -> Pula linha ao terminar o print
"""
```

Exemplos de uso
```py
print("Texto", var) # "Texto var"
print("var =", round(var, x))   # Printa a variável "var" com "x" casas decimais

# Print formatado recebe um f antes das " "
print(f"texto {var}") # "texto var"
print(f"{var:.nf}") # Printa variável float com "n" casas decimais

print("Texto1", var, "\nTexto2")
"""
Texto1 var
Texto2
"""

print("MC102", "UNICAMP", "2022", sep = " - ", end = "!\n")
# "MC102 - UNICAMP - 2022!" e pula linha

# Para printar caracteres especiais, usar o escape (\) antes
print("\\n") # "\n"
print(" \"Frase entre aspas\" ") # " "Frase entre aspas" "
```

## input()
```py
var = input() # Aguarda receber entrada e guarda na variável "var"
"""
A função input() retorna uma string do que foi digitado antes do <ENTER>
"""

var = input("Entrada: ") # Printa o texto e espera por entrada

var = int(input()) # Casting de inteiro no input
```

## range()
```py
# 3 parâmetros
range(inicio, fim, passo)
# 2 parâmetros
range(inicio, fim)  # Por padrão, passo += 1
# 1 parâmetro
range(fim)          # Por padrão, inicio = 0
```

Exemplos de range() com for

```py
for i in range(n): # De 0 até n - 1
    # comando
    # i += 1

for i in range(1, n) # de 1 até n - 1
    # comando
    # i += 1

for i in range(1, n + 1) # de 1 até n
    # comando
    # i += 1

for i in range(1, n, 2) # de 1 até n - 1 ou menor
    # comando
    # i += 2
```

## len()
```py
len(sequencia)
# Retorna a quantidade de elementos de uma sequência
```

## round()
```py
round(var, casas) # Arredonda a variável "var" para um certo número de casas decimais
round(var) # Transforma a variável "var" float em inteiro
```

## min()/max()
```py
min(x1, x2, ..., xn) # Retorna o MENOR valor entre x1, x2, ..., xn
max(x1, x2, ..., xn) # Retorna o MAIOR valor entre x1, x2, ..., xn
```

## sum()
```py
sum(sequencia)
# Retorna a soma de todos os elementos da sequência
```

## type()
```py
type(var) # Retorna o tipo da variável (int, str, float etc)
# Formato: <class 'type'>
```
## exit()
```py
exit(0) # Fecha o programa de forma "amigável" (Por conta do 0)
# Obs: Não utilizar fora do interpretador
```

# Listas, Tuplas, Sets e Dicionários

## Listas (list)

### Criação de listas
```py
listas = [x, y, z]
listas = ["a", "b", "c"]
listas = [x, "a", y, "b", z, "c"]
```
Pela função list()
```py
listas = list() # listas = []
listas = list(range(5)) # listas = [0, 1, 2, 3, 4]
listas = list(["x1", "x2", "x3"]) # listas = [x1, x2, x3]
listas = list("test") # listas = ['t', 'e', 's', 't']
# Strings são listas de caractéres
```
Forma compacta com input
```py
n = int(input())

listas = [int(input()) for i in range(n)]
```

### Operações com listas
```py
lista = [1] * 3 # lista = [1, 1, 1]

lista = [1, 2, 3]
lista2 = lista + [4, 5] # lista2 = [1, 2, 3, 4, 5]
# OU
lista += [4, 5] # lista = [1, 2, 3, 4, 5]
```

### Print de listas
```py
listas = ['A', 'B', 'C', 'D', 'E']

print(listas)  # ['A', 'B', 'C', 'D', 'E']
print(*listas) # A B C D E
```

### Acessar elementos
```py
listas = ['A', 'B', 'C', 'D', 'E']

listas[0]  # 'A'
listas[-1] # 'E'
```

### Alterar elementos
```py
listas = ['A', 'B', 'C', 'D', 'E']

listas[2] = 'x' # listas = ['A', 'B', 'x', 'D', 'E']
```

```py
listas = [0, 1, 2, 3, 4, 5]

listas[1:4] = ['A', 'B', 'C'] # listas = [0, 'A', 'B', 'C', 4, 5]
listas[1:4] = ['A', 'B',] # listas = [0, 'A', 'B', 4, 5]
listas[2:4] = [] # listas = [0, 1, 4, 5]
```

### Verificação de elementos
```py
# Verificar existência
letras = ['A', 'B', 'C', 'D', 'E']

'A' in letras # True
'F' in letras # False
```

### Intervalo de listas (Slice)
```py
listas[start:stop:step]
"""
Começa em start (inclui), termina em stop (exclui) e vai de step em step

Equivale a:
"""

[lista[i] for i in range(início, fim, passo)]

"""
Por padrão
start = 0
stop = len(listas)
step = 1
"""
```
Exemplos de uso
```py
listas = ['A', 'B', 'C', 'D', 'E']

listas[1:3]  # 'B', 'C'
listas[:2]   # 'A', 'B'
listas[-3]   # 'C', 'D', 'E'
listas[::2]  # 'A', 'C', 'E'
listas[1::2] # 'B', 'D'
listas[::-1] # 'E', 'D', 'C', 'B', 'A'
```

### Tamanho de listas len()
```py
listas = ['A', 'B', 'C', 'D', 'E']

len(listas) # 5
```

### Soma de listas
```py
listas = [1, 2, 3, 4, 5]

soma = sum(listas) # soma = 15
```

### Map
```py
map(função, lista)
# Aplica uma função em todos os elementos da lista
```

Casting em listas c/ map()
```py
entrada = ["1", "2", "3", "4", "5"]
entradaInt = list(map(int, entrada)) # [1, 2, 3, 4, 5]
# map aplica int em cada elemento da entrada
# list() aplica list no map
```

## Tuplas (tuple)
```py
# OBS: Tuplas são listas imutáveis, ou seja, uma vez criadas não permitem modificações.
tupla = (x, "y", 11, 10.5)
tupla = x, "y", 11, 10.5

a, b, c, d = tupla # a = x, b = "y", c = 11, d = 10.5
a, *b, c   = tupla # a = x, b = ["y", 11]  , c = 10.5
# OBS: Quando usamos o prefixo *, a variável recebe tudo sobrar das outras

tupla[0] # a
tupla[1] # "b"
print(tupla) # (a, "b")
```

## Sets
```py
# Listas desordenadas e não indexadas, mas são mais rápidos de usar o "in"
sets = {x, "y", 11, 10.5}
```

### Operações matemáticas
Operações matemáticas podem ser feitas entre sets, gerando outro set. Elas são:

    | -> União
    & -> Intersecção
    - -> Diferença (Itens da esquerda - itens da direita)
    ^ -> Diferença Simétrica (Itens que só estão em um ou outro, não ambos)

## Dicionários (dict)
```py
dicionario = {
    key: value,
    a: "b",
    "c": d
}
# OBS: A key tem que ser algo imutável

dicionario[key] # value
dicionario[a]   # "b"
dicionario["c"] # d
print(dicionario) # {key: value, a: "b", "c": d}
```

# Métodos

## Class String

### Operações com strings
```py
"Texto1" + "Texto2" # "Texto1Texto2"
"A" * 3 # "AAA"
"1" + "1" # "11"

"a" < "b" # True
# Ordem do alfabeto: ABC...XYZabc...xyz
```
### Verificação de ocorrência
```py
string = "Olá mundo"
"Ol" in string # True
"Do" in string # False (Case sensitive)

.startswith("Olá") # True
.startswith("mundo") # False
```

### Acessar elementos
```py
string[x] # Acessa o índice x da string
string[start:stop:step] # String c/ slice
# Vai de start até stoop - 1 de step em step
# Por padrão: start = 0; stop = len(string); step = 1
```

```py
.index() # Retorna o index que começa o argumento
.find() # Retorna o index que começa o argumento, retorna -1 caso não encontre
```

### Formatação
```py
.capitalize() # Inicial maiúscula
.upper() # Todas maiúsculas
.lower() # Todas minúsculas
```
```py
.strip() # Retira espaços, \n etc das extremidades
.replace("x", "y") # Retorna a string com os "x" trocados por "y"
.split(separador) # Transforma uma string em uma lista de strings, separando pelo separador
# Por padrão, separador = " " -> Espaço
```
```py
"{0} {1}".format(var0, var1) # Coloca as variáveis do argumento em ordem nos placeholders {n}
"{const}".format(const = x) # Outra forma de usar
# OBS: Usada semelhantemente no print formadato de uma forma mais direta como: print(f"")
```

## Class List

### Adicionar elementos
```py
.insert(index, elemento) # Adiciona o elemento na posição do Index

.append(elemento) # Adiciona o elemento no fim da lista

.extend(lista) # Adiciona elementos da lista "lista" no fim da lista "listas"
```

### Remover elementos
```py
.remove(elemento) # Remove a 1a ocorrência do elemento
# OBS: Se o elemento não estiver na lista, haverá um erro

.pop(indice) # Retorna elemento do índice e o remove da lista
```

### Verificiar ocorrência
```py
.index(elemento) # Retorna o índice do elemento
```

### Contagem de ocorrência
```py
.count(elemento) # Retorna o n° de ocorrências do elemento
```

### Ordenação de listas
```py
.sort() # Ordenada em ordem Crescente

.sort(reverse = True) # Ordena em ordem Decrescente

listas.reverse() # Inverte ordem da lista
```

### Cópia de listas
```py
listas2 = listas.copy()  # Cópia independente da lista
listas2 = sorted(Listas) # Cópia ordenada da lista, sem alterar original
```

### Join
```py
# Transforma uma lista de strings em uma string
string = sep.join(listas)
# sep = separador entre os elementos da lista
```

## Class Set

### Adicionar/Remover elementos
```py
.add(elemento) # Adiciona um elemento
.remove(elemento) # Remove um elemento
```

# Inclusão de bibliotecas

```py
import Nome_da_biblioteca # Importa uma biblioteca
import Nome_da_biblioteca as prefix # Importa uma biblioteca com um prefixo diferente
from Nome_da_biblioteca import something # Importa algo específico de uma biblioteca
```
Exemplos de uso
```py
import math

x = math.pi
```
```py
from math import pi

x = pi
```
```py
import math as m

x = m.pi
```
# Funções importantes
