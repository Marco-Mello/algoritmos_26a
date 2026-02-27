# Lista 7B

**Nome:**

---

## Q1

Analise o algoritmo a seguir. Justifique sua corretude e analise o tempo de execução.  
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, use a notação O com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre dois elementos distintos em valor absoluto**

- **INPUT:** Um vetor `A[1...n]` de n inteiros distintos, com `n ≥ 2`  
- **OUTPUT:** `min₁ ≤ i < j ≤ n|A[i] - A[j]|`

```pseudo
Ordene A em ordem crescente usando MERGESORT
menorDif ← |A[2] - A[1]|

para i ← 2 até n-1 faça
    dif ← |A[i+1] - A[i]|
    se dif < menorDif então
        menorDif ← dif
    fim se
fim para
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: TriplaSoma**

- **INPUT:** Um vetor `A[1...n]`

```pseudo
se n ≤ 1 então retorna A[1]

m ← ⌊n/2⌋

x ← TriplaSoma(A[1...m])
y ← TriplaSoma(A[m + 1...n])
z ← TriplaSoma(A[1...m])

soma ← 0
para i ← 1 até 4 faça
    para j ← 1 até n faça
        soma ← soma + A[j]
    fim para
fim para

retorna x + y + z + soma
```

---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

**(a)**  
`10n² + 100n - 1` é `O(g(n))` para qual `g(n)`?

**(b)**  
`20n³ - 10n + 100` é `Ω(g(n))` para qual `g(n)`?

---

## Q4

Responda cada item e justifique.

**(a)**  
Bob está analisando dois algoritmos:
- O algoritmo A tem tempo de execução `O(n²)`
- O algoritmo B tem tempo de execução `O(n³)`

Ele afirma que, em teoria, o algoritmo A é mais eficiente que o B.  
Ele está correto?

**(b)**  
Se `f(n) = O(g(n))` e `h(n) = Ω(g(n))`, é verdade que  
`[f(n) + h(n)]/2  = ϴ(g(n))`?

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema. Escreva um pseudocódigo e justifique brevemente sua corretude. O seu algoritmo deve dividir o vetor em duas partes.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** A soma dos elementos pares de `A`, ou seja, Σᵢ∈I A[i] tal que I = {I : A[1] é par}
