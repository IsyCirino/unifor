# UNIFOR
**Nome**: Nome do estudante <br>
**Disciplina**: Raciocínio lógico algorítm

## Exercício exemplo 1
Implemente e teste um programa que imprima os n primeiros números.

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[\n\]
C --> D[\num = 1\]
D --> E{num <= n}
E --FALSE--> I([FIM])
E --TRUE--> F{{"Num", num}}
F --> G[num =+ 1]
G --LOOP--> E
```

#### Pseudocódigo
```
1 ALGORITMO print_n_primeiros
2 DECLARE n, num: INTEIRO
3 INICIO
4 ESCREVA “Digite um número: ”
4 LEIA n			// variável de entrada n
4 num ← 1			// variável num inicializada
5 ENQUANTO num <= n FAÇA	// n iterações
7	ESCREVA “Número ”, num
8	num ← num + 1		// num =+ 1 (incremento)
8 FIM_ENQUANTO
9 FIM
```

#### Teste de mesa
| it | n  | num | num <= n | Saída      | num =+ 1 |
| -- | -- | --  | --       | --         | --       |
| 1  | 10 | 1   | True     | Número 1   | 2        |
| 2  | 10 | 2   | True     | Número 2   | 3        |
| 3  | 10 | 3   | True     | Número 3   | 4        |
| 4  | 10 | 4   | True     | Número 4   | 5        |
| 5  | 10 | 5   | True     | Número 5   | 6        |
| 6  | 10 | 6   | True     | Número 6   | 7        |
| 7  | 10 | 7   | True     | Número 7   | 8        |
| 8  | 10 | 8   | True     | Número 8   | 9        |
| 9  | 10 | 9   | True     | Número 9   | 10       |
| 10 | 10 | 11  | True     | Número 10  | 11       |
| 11 | 10 | 11  | False    |            |          |

## Exercício exemplo 2
Implemente e teste um programa que some os n primeiros números.

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[\n\]
C --> D[\soma = 0\]
D --> E[[i=1 ATÉ n PASSO 1]]
E --FALSE--> G([FIM])
E --TRUE--> F[soma =+ i]
F --LOOP--> E
```

#### Pseudocódigo
```
1  ALGORITMO	soma_n_numeros()
2  DECLARE	n, i, soma: INTEIRO
3  INICIO
4  ESCREVA “Digite a quantidade de números: ”
5  LEIA n		// variável de entrada n
7  soma ← 0		// variável soma inicializada
6  PARA i DE 1 ATÉ n PASSO 1 FAÇA
7	soma ← soma + i	// soma =+ i (incremento)
8  FIM_PARA
9  ESCREVA “A soma é igual a ”, soma
10 FIM
```

#### Teste de mesa
| it | n  | soma | i  | soma =+ i |
| -- | -- | --   | -- | --        |
| 1  | 10 | 0    | 1  | 1         |
| 2  | 10 | 1    | 2  | 3         |
| 3  | 10 | 3    | 3  | 6         |
| 4  | 10 | 6    | 4  | 10        |
| 5  | 10 | 10   | 5  | 15        |
| 6  | 10 | 15   | 6  | 21        |
| 7  | 10 | 21   | 7  | 28        |
| 8  | 10 | 28   | 8  | 36        |
| 9  | 10 | 36   | 9  | 45        |
| 10 | 10 | 45   | 10 | 55        | 

## Lista de exercícios 03

### Exercício 01 (2.5 pontos)
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero. 

#### Fluxograma
``` mermaid
flowchart TD
A([Início])-->B{{Digite um número inteiro positivo: }}
B--> C[/n/]
C-->D{n<0}
D--> |não|F[resto = n%2]
F-->G{{resto==0}}
G-->|sim|H{{O número digitado é par}}
G-->|não|I{{O número digitado é impar}}
D-->|sim|E{{O número digitado é negativo, tente de novo!}}
E-->|loop|B
I-->J([Fim])
H-->J
```
#### Pseudocódigo
```
Algorítmo impar_par_loop:
DECLARE n,resto: INTEIRO
INÍCIO:
ESCREVA "Digite um número inteiro positivo:"
LEIA n
ENQUANTO n<0 FAÇA
	ESCREVA "o número digitado é negativo. Tente de novo!"
FIM_ENQUANTO
resto <- n%2
SE resto == 0 ENTÃO
	ESCREVA"O número digitado é par."
SENAO
	ESCREVA"o número digitado é impar."
FIM_SE
FIM
```
####  Teste
| n |n<0| resto | resto=0| Saída|
| -- | -- | -- | -- | --|
|-1| T| | |O número digitado é negativo. Tente de novo! | 
|4| F |0|T| O número digitado é par.|
|5| F |1|F|O número digitado é impar. |

### Exercício 02 (2.5 pontos)
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[[i de 0 até 30 passo 3]]
B-->|Verdadeiro|C{{i}}
B--> |Falso|D([Fim])
C-->|loop|B

```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo mutiplos_3
DECLARE i : INTEIRO
INÍCIO:
PARA i DE 0 ATE 30 PASSO 3 FAÇA
	ESCREVA i
FIM_PARA
FIM
```

#### Teste de mesa (0.5 ponto)

| i | Saída|
|      --      |      --      |     
| 0 | 0 |  
| 3 | 3 |  
| 6 | 6 |  
| 9 | 9 |  
| 12 | 12 |  
| 15| 15 |  
| 18 | 18 |  
| 21 | 21 |
| 24 | 24 |  
| 27 | 27 |  
| 30 | 30|  

### Exercício 03 (2.5 pontos)
Dada uma sequência de números inteiros, calcular a sua soma. 
Por exemplo, para a sequência {12, 17, 4, -6, 8, 0}, o seu programa deve escrever o número 35.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite um número qualquer (0 para parar): "}}
B-->C[/n/]
C-->D[/sum=0/]
D-->E{n!=0}
E-->|sim|F[sum+=n]
F-->|loop|E
E-->|não|G{{A soma foi, sum}}
G-->H([Fim])



```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo soma_valores
DECLARE n,sum : REAL
INÍCIO:
ESCREVA "Digite um número qualquer (0 para parar)"
LEIA n
sum <- 0
ENQUANTO n!=0 FAÇA
	sum+=n
FIM_ENQUANTO
ESCREVA "A soma foi: ", sum
FIM
```

#### Teste de mesa (0.5 ponto)

| n| sum| n!=0| Saída|
|      --      |      --      |      --      |       --      |  
| 12| 12| T| |
| 17| 29|T| |
| 4| 33| T| |
| -6| 27| T||
| 8| 35|T| |
 |0| 35|F| 35|

### Exercício 04 (2.5 pontos)
Escreva um programa que leia a nota de diversos alunos, até que seja digitada uma nota negativa. 
Nesse momento, ele mostra a média aritmética de todas as notas lidas e quantas notas foram lidas. 
Ex. Foram lidas 14 notas. A média aritmética é 6.75!

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[/cont=1, sum=0/]
B-->C{{Digite a nota,cont:}}
C-->D[/n/]
D-->E{n<0}
E-->|verdadeiro|F[media=sum/cont]
F-->H{{Foram,cont, notas e sua média foi,media. }}
E-->|falso|G[cont+=1 e sum+=n]
G-->C
H-->I([fim])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo media_cont_notas
DECLARE sum,n: REAL
DECLARE cont: INTEIRO
INÍCIO:
sum <-0
cont <-1
n <-0
ENQUANTO n>=0 FAÇA
	ESCREVA "Digite nota",cont,":"
	LEIA n
	sum+=n
	cont+=1
FIM_ENQUANTO
ESCREVA "A Foram",cont, "notas e sua média foi",media"." 
FIM
```

#### Teste de mesa (0.5 ponto)

| n|n>=0 | cont| sum |Saída|
|      --      |      --      |      --      |       --      |   --      |  
| 5| T| 1| 5|
| 17| T|2|22|
| 4| T| 3| 26 |
| -6| F|3 |26|"A Foram 3 notas e sua média foi 8,666666 |
