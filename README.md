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

print(f"var = {var:.xf}")       # Printa a variável "var" com "x" casas decimais
print("var =", round(var, x))   # Printa a variável "var" com "x" casas decimais

var = input() # Aguarda receber entrada
var = input("Texto") # Printa o texto e espera por entrada
var = int(input()) # Casting de inteiro no input (String por padrão) 

if condição:
    # comando (PRECISA DE IDENTAÇÃO)
elif: # Equivalente ao else if
    # comando (PRECISA DE IDENTAÇÃO)
else:
    # comando (PRECISA DE IDENTAÇÃO)
# Na condição, qualquer expressão que tenha um valor != 0 é considerada True

a if condição else b

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

```py
# 3 parâmetros
range(inicio, fim, passo)
# 2 parâmetros
range(inicio, fim)  # Por padrão, passo += 1
# 1 parâmetro
range(fim)          # Por padrão, inicio = 0
```

Exemplos de for com range()

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

```py
round(var, casas) # Arredonda a variável "var" para um certo número de casas decimais
round(var) # Transforma a variável "var" float em inteiro

min(x1, x2, x3) # Retorna o MENOR valor entre x1, x2 e x3
max(x1, x2, x3) # Retorna o MAIOR valor entre x1, x2 e x3

type(var) # Retorna o tipo da variável (int, str, float etc)
# Formato: <class 'type'>

exit(0) # Fecha o programa de forma "amigável" (Por conta do 0)
# Obs: Não utilizar fora do interpretador
```

### Tipos de dados

```py
int = 11 # Inteiro
float = 11.10 # Float (Números decimais)
str = "Enzo" # String (Texto)
bool = True # Booleana (True ou False)
```
Conversão
```py
a = "1"
b = "1"
resultado = int(a) + int(b) # resultado = 2 ao invés de "11"

# Com bool(), qualquer número != 0 e qualquer string != "" resultam em True
```

### Operadores

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

### Atribuição de variável

```py
x = 10 # Atribui 10 a "x"
x, y = 10, 20 # Atribui 10 a "x" e 20 a "y"

# Obs: Python é case sensitive
```

### Concatenação de String

```py
"Texto1" + " Texto2" = "Texto1 Texto2"
"A" * 3 = "AAA"
"1" + "1" = "11"

"a" < "b" = True
# Ordem do alfabeto: ABC...XYZabc...xyz
```

## Listas

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

Alterar elementos com intervalos

```py
listas = [0, 1, 2, 3, 4, 5]

listas[1:4] = ['A', 'B', 'C'] # listas = [0, 'A', 'B', 'C', 4, 5]
listas[1:4] = ['A', 'B',] # listas = [0, 'A', 'B', 4, 5]
listas[2:4] = [] # listas = [0, 1, 4, 5]
```

### Adicionar elementos

```py
listas.insert(pos, elemento) # Insere um elemento na pos (não remove nenhum elemento)
listas.append(elemento) # Adiciona o elemento no final da lista
```
```py
listas = [0, 1, 2, 3]

listas.insert(0, 'x') # listas = ['x', 0, 1, 2, 3]
listas.append('x') # listas = [0, 1, 2, 3, 'x']
```

### Verificação de elementos

```py
letras = ['A', 'B', 'C', 'D', 'E']

'A' in letras # True
'F' in letras # False
```

### Intervalo de listas

```py
listas[start:stop:step]
# Começa em start (inclui), termina em stop (exclui) e vai de step em step

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

### Ordenação de listas

```py
listas.sort() # Aceita 2 argumentos

listas.sort()               # Ordem crescente
listas.sort(reverse = True) # Ordem decrescente
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