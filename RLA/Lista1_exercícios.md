# UNIFOR
**Nome**: Ian Cirino <br>
**Disciplina**: Raciocínio lógico e algorítmo
## Lista de exercícios 1
### Exercício 2
represente, em fluxograma e em pseudocódigo, para calcular a média aritmética entre
duas notas de um aluno e mostrar sua situação, que pode ser aprovado ou reprovado
#### Fluxograma
``` mermaid
flowchart TD
A([Início])-->B{{Digite nota 1}}
B--> C[/leia a nota 1/]
C--> D{{Digite nota 2}}
D--> E[/leia nota 2/]
E--> F["Média=(Nota1 + Nota2)/2"]
F--> G{M>=7}
G-->|verdadeiro|H[/O aluno foi aprovado/]
G-->|Falso|I[/O aluno foi reprovado/]
H--> J([Fim])
I--> J
### Exercício 3
represente, em fluxograma e em pseudocódigo, um algoritmo para determinar se o número inteiro é par ou impar
#### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{Digite o número:}}
-->C[/N/]
C--> T{N>=0}
T-->|Falso|J([Digite um número positivo])
J-->H
T
-->|Verdadeiro|D[R=N%2]-->E{R=0}-->|Sim|F{{O número é par}} 
E-->|Não|G{{O número é impar}}
G-->H([Fim])
F-->H([Fim])
```
#### Pseudocódigo

``` 
ALGORITMO verificar_par_impar:
DECLARE num, resto: INTEIRO
INICIO:
ESCREVA"Digite o nùmero:"
LEIA num
SE num>=0 ENTÃO
	resto <- num%2
	SE resto == 0 ENTÃO
		ESCREVA"O nùmero è par"
	SENAO
		ESCREVA"O nùmero è impar"
	FIM_SE
SENAO
	 ESCREVA "O nùmero deve ser positivo"
FIM_SE
FIM
```
#### Teste
| num |  num>=0 | resto | resto == 0 | saída |
| -- | -- | -- | -- | -- |
|-1| False| | | O número deve ser positivo|
|0| True | 0| True| O número é par|
|10|True|0|True| O número é par|
|11|True|1|False|O número é impar|

