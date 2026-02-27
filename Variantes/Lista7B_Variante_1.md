
# Lista 7B - Variante 1

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre dois elementos distintos em valor absoluto**

- **INPUT:** Um vetor `A[1..n]` de inteiros distintos, com `n ≥ 2`
- **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|`

Ordene **A** em ordem crescente usando **MERGESORT**.

```pseudo
menorDif ← |A[2] - A[1]|
para i ← 2 até n-1 faça
    dif ← |A[i+1] - A[i]|
    se dif < menorDif então
        menorDif ← dif
    fim se
fim para
retorne menorDif
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.
(Não é preciso resolver nem justificar.)

**Algoritmo 2: TriplaSoma**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza:

- Três chamadas recursivas:
  - `x = TriplaSoma(A[1..m])`
  - `y = TriplaSoma(A[m+1..n])`
  - `z = TriplaSoma(A[1..m])`
- Dois laços aninhados que executam 4 × n operações no total em cada nível.

Escreva a recorrência para `T(n)`.

---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e valor de `n₀`.

**(a)**  
`10n² + 100n - 1` é `O(g(n))` para qual `g(n)`?

**(b)**  
`20n³ - 10n + 100` é `Ω(g(n))` para qual `g(n)`?

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Bob está analisando dois algoritmos:

- Algoritmo A possui tempo de execução `O(n²)`
- Algoritmo B possui tempo de execução `O(n³)`

Ele afirma que, em teoria, o algoritmo A é mais eficiente que o algoritmo B para entradas suficientemente grandes.  
Ele está correto? Justifique rigorosamente.

**(b)**  
Se `f(n) = O(g(n))` e `h(n) = Ω(g(n))`, é verdade que

```
(f(n) + h(n)) / 2 = Θ(g(n))
```

Justifique formalmente ou apresente um contraexemplo.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos
- **OUTPUT:** Soma dos elementos pares de `A`

Requisitos:

- Caso base claramente definido.
- Divisão explícita em duas metades.
- Combinação correta dos resultados parciais.
- Justificativa breve da corretude.

---

**Instruções:** Mostre todos os passos, desigualdades e transformações quando fizer provas assintóticas.
