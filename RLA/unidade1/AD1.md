<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Engenharia da Computação <br>
**Disciplina:** Raciocínio lógico e algorítmo <br>
**Código/Turma:** T998-08 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** 20/03/2024 <br>
**Aluno(a):** Ian Carvalho Cirino <br>
**Matrícula:** 2410304 <br>

**1a chamada (Sim/Não):** sim <br>
**2a chamada (Sim/Não):** não

# Avaliação Diagnóstica 1

## Normas e exigências

Avaliação diagnóstica (**AD**) consiste em exercícios ou projetos desenvolvidos em grupo ao longo da disciplina. <br>
A primeira avaliação diagnóstica (**AD1**) será composta por exercícios e equivale a 30% da nota da primeira avaliação (**AV1**).

Segue abaixo a expressão para o cálculo da **AV1**, sendo sendo **AF1** equivale a primeira avaliação formativa e **AD1**, a primeira avaliação diagnóstica.

$$AV_1 = AF_1 \times 0,30 + AD_1 \times 0,70$$

A **AD1** é formada pela entrega dos exercícios (**EX1**) na data prevista e apresentação (**AP1**) de um dos exercícios escolhido pelo professor.
Segue abaixo a expressão para o cálculo da **AD1**.

$$AD_1 = (EX1_1 + AP_1)/2 $$

A **EX1** é avaliada mediante a **correção dos exercícios**, sendo a avaliação no intervalo de 0% (não atende a questão), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se o exercício equivale a 2 pontos e sua correção atente parcialmente a questão, então sua avaliação deste exercício será 1 ponto.

A **AP1** é avaliada mediante aos pré-requisitos de **clareza, organização e domínio do conteúdo**. Portanto, o aluno deve demonstrar um bom entendimento do algoritmo, explicando seus princípios fundamentais, seu propósito e como ele funciona passo a passo. <br>

A avaliação da **AP1** é apenas considerada no intervalo de 0% (não atende os pré-requisitos), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se na apresentação do exercício, o aluno atenter parcialmente os pré-requisitos, então sua avaliação da apresentação será 5,0.

## Datas
- Entrega da primeira avaliação formativa (**AF1**) composta pelas listas de exerciícios 1, 2 e 3: 21/03/24
- Entrega dos exercícios da primeira avaliação diagnóstica (**EX1**): 21/03/24
- Apresentação da primeira avaliação diagnóstica (**AP1**): 21/03/24

## Lista de questões

### Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis, $a$ e $b$, implemente e teste um algoritmo para trocar os valores atribuídos a elas.

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o valor de a: }}
B-->C[/a/]
C-->D{{Digite o valor de b: }}
D-->E[/b/]
E-->F[/c=b/]
F-->G[b=a]
G-->H[a=c]
H-->I{{a =,a, b = ,b}}
I-->J([Fim])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo TrocaValores
DECLARE a,b,c : REAL
INÍCIO:
ESCREVA "Digite o valor de a: "
LEIA a
ESCREVA "Digite o valor de b: "
LEIA b
c <- b
b <- a
a <- c
ESCREVA "a = ",a," b = ",b
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| a | b | c | a | b | Saída|
|      --      |      --      |      --      |      --      |      --      |   --      | 
| 1  | 2 | 2   |  2     |1  |  a = 2 b = 1 |
| 4|3|3    | 3 | 4| a = 3 b = 4
### Questão 2 - Contagem (1 ponto)

Dado um conjunto $n$ de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem $cont$ do número de alunos que foram aprovados no exame. 
Será considerado aprovado o aluno que tirar $nota$ 50 ou maior (no intervalo de 0 a 100).


#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o número de notas: }}
B-->C[/n/]
C-->H[/contA=0/]
H-->D[[i ATÉ n PASSO 1]]
D-->|verdadeiro|E{{Digite nota, i:}}
E-->F[/nota/]
F-->G{nota>=50}
G-->|sim|I[contA+=1]
G-->|não|D
I-->|loop|D
D-->|falso|S{{contA, alunos foram aprovados!}}
S-->R([Fim])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo ContaAprovacoes
DECLARE n,i,contA: INTEIRO
DECLARE nota: REAL
INÍCIO:
ESCREVA"Digite o número de notas: "
LEIA n
contA <- 0
PARA i DE 1 ATÉ n PASSO 1 FAÇA
	ESCREVA"Digite nota ",i," :"
	LEIA nota
	SE nota>=50 ENTÃO
		contA <- contA + 1
	FIM_SE
FIM_PARA
ESCREVA contA," alunos foram aprovados!"
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | i | nota | nota>=50 | Saída | 
|      --      |      --      |      --      |      --      |      --      | 
| 3   | 1      | 30   |  F   |   |
| -  | 2          | 50        | T |   |
| -  | 3        | 70        | T | 2 alunos foram aprovados!  |

### Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de $n$ números, implemente e teste um algoritmo para calcular a soma desses números. <br>
Aceite apenas $n$ maior ou igual a zero.

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a quantidade de números: }}
B-->C[/n/]
C-->D{n<0}
D-->|sim|E{{Digite um valor positivo}}
E-->|loop|B
D-->I[sum=0]
I-->|não|F[[i DE 1 ATÉ n PASSO 1]]
F-->|verdadeiro|G{{Digite um número qualquer:}}
G-->H[/num/]
H-->J[sum+=num]
J-->|loop|F
F-->|falso|K{{soma dos números igual à: , sum}}
K-->L([FIM])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo SomaNúmeros
DECLARE i,n: INTEIRO
DECLARE num: REAL
INÍCIO:
ENQUANTO VERDADEIRO FAÇA
	ESCREVA "Digite a quantidade de números: "
	LEIA n
	SE n<0 ENTÃO
		ESCREVA"Digite um valor positivo!"
	SENAO
		QUEBRE_LOOP
	FIM_SE
FIM_ENQUANTO
sum <- 0
PARA i DE 1 ATÉ n PASSO 1 FAÇA
	ESCREVA"Digite um número qualquer"
	LEIA num
	sum <- sum + num
FIM_PARA
ESCREVA "A soma dos números foi ", sum
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | n<0 | i | num | Saída | 
|      --      |      --      |      --      |      --      |      --      | 
| -2  | T    | 0   |  -   | Digite um valor positivo!  |
| 3 | F         | 1     | 5.5 |   |
| -  | -        | 2      |9|   |
| -  | -        | 3      | -1.5| A soma dos números foi 13 |

### Questão 4 - Cálculo de uma série (1 ponto)

Dado um conjunto de $n$ termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

$$ S = \frac{1}{2} + \frac{3}{4} + \frac{5}{6} + \frac{7}{8} + \dots $$


#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a quantidade de termos: }}
B-->C[/n/]
C-->F[/sum = 0/]
F-->D[[i DE 1 ATÉ n PASSO 2]]
D-->|verdadeiro|E["sum+=i/(i+1)"]
E-->|loop|D
D-->|falso|G{{A soma da serie de termos resulta em ,sum}}
G-->L([Fim])

```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo SerieTermos
DECLARE i,n: INTEIRO
DECLARE sum: REAL
INÍCIO:
ESCREVA"Digite a quantidade de termos: "
LEIA n
sum <- 0
PARA i DE 1 ATÉ n PASSO 2 FAÇA
	sum <- sum + i/(i+1)
FIM_PARA
ESCREVA "A soma da serie de termos resulta em ",sum
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | i | sum | Saída | 
|      --      |      --      |      --      |      --      |    
| 3 | 1   | 0   |  -   | -  |
| - |1       | 0.5    |  
|  -|2       | 1.25    |  
| - | 3        |2.125     | A soma da serie de termos resulta em 2.125
### Questão 5 - Cálculo fatorial (2 pontos)

Dado um número $n$, implemente e teste um algoritmo para calcular o fatorial de $n$ (escrito como $n!$), onde $n ≥ 0$.


#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número inteiro positivo n: }}
B-->C{n>=0}
C-->|não|D{{Número inválido. Tente novamente!}}
D-->|loop|B
C-->|sim|E[fat=1]
E-->F[[i DE 1 ATÉ n PASSO 1]]
F-->|verdadeiro|G[fat*=i]
G-->|loop|F
F-->|falso|H{{O fatorial de ,n, é ,fat}}
H-->L([Fim])


```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo Fatorial
DECLARE i,n,fat: INTEIRO
INÍCIO:
ESCREVA"Digite um número inteiro positivo n: "
LEIA n
ENQUANTO n<0 FAÇA
	ESCREVA"Número inválido. Tente novamente!"
	ESCREVA"Digite um número inteiro positivo n: "
	LEIA n
FIM_ENQUANTO
fat <- 1
PARA i DE 1 ATÉ n PASSO 1 FAÇA
	fat <- fat*i
FIM_PARA
ESCREVA"O fatorial de ",n," é: ",fat
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | n<0 |i| fat| Saída | 
|      --      |      --      |      --      |      --      |     --      |    
| -2| T  | 1  | 1  | Número inválido. Tente novamente! |
| 4| F  | 1  | 1  |  |
| 4| F | 2  | 2  | |
| 4|F | 3  | 6  | |
| 4| F  | 4  | 24  | O fatorial de 4 é: 24|

### Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os $n$ primeiros termos da sequência de Fibonacci, onde $n ≥ 1$. <br>
Os primeiros termos são: $0, 1, 1, 2, 3, 5, 8, 13, \dots$ <br>
Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.


#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número inteiro positivo n: }}
B-->K[/n/]
B-->C{n>=1}
C-->|não|D{{número inválido. Tente novamente!}}
D-->|loop|B
C-->|sim|E[/termoA = 0, termoB=1/]
E-->F[[i DE 0 ATÉ n PASSO 1]]
F-->|verdadeiro|G{{termoA}}
G-->H[termoA+=termoB]
H-->I[termoB+=termoA]
I-->|loop|F
F-->|falso|J([Fim])


```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo Fibonacci
DECLARE i,n,termoA,termoB: INTEIRO
INÍCIO:
ESCREVA"Digite um número inteiro positivo n: "
LEIA n
ENQUANTO n<1 FAÇA
	ESCREVA"Número inválido. Tente novamente!"
	ESCREVA"Digite um número inteiro positivo n: "
	LEIA n
FIM_ENQUANTO
termoA <- 0
termoB <- 1
PARA i DE 1 ATÉ n PASSO 1 FAÇA
	ESCREVA "",termoA,""
	ESCREVA "", termoB,""
	termoA <- termoA + termoB
	termoB <- termoB + termoA
FIM_PARA
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | n<1 |i| termoA| termoB| Saída|
|      --      |      --      |      --      |      --      |     --      |     --      |    
| 0| T  | 0  | 0 | 1 |Número inválido. Tente novamente!|
| 4| F  | 0  | 0 | 1 |0|
| 4| F  | 1  | 1 | 1 |1|
| 4| F  | 2  | 1| 2|1|
| 4| F  | 3  | 2 | 3| 2|

### Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Implemente e teste um algoritmo para inverter a ordem dos dígitos de um número inteiro positivo de dois dígitos.


#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número inteiro: }}
B --> C[\num\]
C --> D{num >= 0}
D --TRUE--> G[num_inv = 0]
G --> H{num > 0}
H --FALSE--> Z{{"Número invertido:", numero_inv}}
Z --> W([FIM])
H --TRUE--> I[digito = num % 10]
I --> J[num_inv = num_inv * 10 + digito]
J --> K[numero = numero // 10]
K --LOOP--> H
D --FALSE--> E{{O número deve ser positivo!}}
E --> W
```

#### Pseudocódigo (0.5 pontos)
``` 
Algoritmo inversãoDigitos
DECLARE num, numInverso, digito: INTEIRO
INÍCIO:
ESCREVA"Digite um número inteiro positivo:"
LEIA num
SE num<0 ENTÃO
	ESCREVA"O número deve ser inteiro positivo"
SENAO
	numInverso <- 0
	ENQUANTO num>0 FAÇA
		digito <- num%10
		numInverso <- numInverso*10 + digito
		num <- num//10
	FIM_ENQUANTO
	ESCREVA"O inverso do número é ",numInverso
FIM_SE
FIM_ALGORITMO
```

#### Teste de mesa

| it | num | num_inv | num > 0 | digito | num = num // 10 | num_inv = (num_inv * 10) + digito | Saída                       |
| -- | --  | --      | --     | --      | --              | --                                | --                          |
|    | -1  | 0       | False  |         |                 |                                   | O número deve ser positivo! |
| 1  | 0   | 0       | False  |         |                 |                                   | Número invertido:: 0        |
| 1  | 42  | 0       | True   | 2       | 4               | 2                                 |                             |
| 2  | 4   | 2       | True   | 4       | 0               | 24                                |                             |
| 3  | 0   | 24      | False  |         |                 |                                   | Número invertido:: 24       |
