# Estudos em Python
- ### [Udemy](https://www.udemy.com/course/curso-algoritmos-logica-de-programacao/)

# Lembretes
## Syntax

```py
# Comentários na linha utilizam "#"

"""
Comentários em várias linhas
utilizam no início e fim 3 aspas seguidas
"""

print(var) # Printa uma variável
print("Hello, World!") # Printa um texto

print("Texto", var) # Printa texto seguido de variável
print(f"texto{var}") # Printa texto seguido de variável

print(f"{var:.nf}") # Printa variável float com "n" casas decimais

print("Texto1", var, "\nTexto2") # Printa texto seguido de quebra de linha seguido de outro texto
print("MC102", "UNICAMP", "2022", sep = " - ", end = "!\n") # Printa "MC102 - UNICAMP - 2022!" e pula linha
# Por padrão, sep = " " e end = "\n"
print("\\n") # Printa \n (Não quebra linha)

var = input() # Aguarda receber entrada
var = input("Texto") # Printa o texto e espera por entrada
var = int(input()) # Casting de inteiro no input (String por padrão) 

if condição:
    # comando (PRECISA DE IDENTAÇÃO)
elif: # Equivalente ao else if
    # comando (PRECISA DE IDENTAÇÃO)
else:
    # comando (PRECISA DE IDENTAÇÃO)

type(var) # Retorna o tipo da variável (int, str, float etc)
```

### Tipos de dados

```py
int = 11 # Inteiro
float = 11.10 # Float (Números decimais)
str = "Enzo" # String (Texto)
bool = True # Booleana (True ou False)
```
Casting
```py
resultado = int(a) + int(b)
```

### Operadores

    +  -> Adição
    -  -> Subtração
    *  -> Multiplicação
    /  -> Divisão
    // -> Divisão Inteira
    %  -> Resto da divisão
    ** -> Potenciação

    += -> Incrementa
    -= -> Decréscimo

### Atribuição de variável

```py
x = 10 # Atribui 10 a "x"
x, y = 10, 20 # Atribui 10 a "x" e 20 a "y"

# Obs: Python é case sensitive
```

## Inclusão de bibliotecas

```py
import nomeDaBiblioteca
from nomeDaBiblioteca import funcaoEspecifica
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

## Funções importantes