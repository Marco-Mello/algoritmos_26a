# Lista 7B - Variante 10

**Nome:**

------------------------------------------------------------------------

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude
(explique por que o algoritmo resolve corretamente o problema proposto)
e analise o tempo de execução.\
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível,
utilize notação **O** com uma análise justa (sem folga) para o pior
caso.

**Algoritmo 1: Maior diferença entre dois elementos distintos em valor
absoluto**

-   **INPUT:** Um vetor `A[1...n]` de n inteiros distintos, com `n ≥ 2`\
-   **OUTPUT:** `max₁ ≤ i < j ≤ n |A[i] - A[j]|`

``` pseudo
Ordene A em ordem crescente usando MERGESORT
maiorDif ← |A[n] - A[1]|
retorne maiorDif
```

------------------------------------------------------------------------

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a
seguir.\
(Não é preciso resolver nem justificar.)

**Algoritmo 2: SomaDuplicada**

-   **INPUT:** Um vetor `A[1...n]`

``` pseudo
se n ≤ 1 então retorna A[1]

m ← ⌊n/2⌋

x ← SomaDuplicada(A[1...m])
y ← SomaDuplicada(A[m + 1...n])

soma ← 0
para i ← 1 até 3 faça
    para j ← 1 até n faça
        soma ← soma + A[j]
    fim para
fim para

retorna x + y + soma
```

------------------------------------------------------------------------

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico
**(justo, sem folga)** e prove.

**(a)**\
`15n² + 200n + 50` é `O(g(n))` para qual `g(n)`?

**(b)**\
`50n³ + 10n² - 7` é `Ω(g(n))` para qual `g(n)`?

------------------------------------------------------------------------

## Q4

Responda cada item e justifique formalmente.

**(a)**\
Considere dois algoritmos: - Algoritmo A possui tempo `O(n log n)` -
Algoritmo B possui tempo `O(n²)`

Em teoria, A é mais eficiente que B para entradas suficientemente
grandes? Justifique.

**(b)**\
Se `f(n) = Θ(g(n))` e `h(n) = O(g(n))`, é necessariamente verdade que\
`f(n) - h(n) = Ω(g(n))`?

------------------------------------------------------------------------

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte
problema.\
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.\
O algoritmo deve dividir o vetor em duas partes em cada chamada
recursiva.

-   **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos\
-   **OUTPUT:** A soma dos elementos ímpares de `A`
