# Lista 7B - Variante 2

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Maior diferença entre dois elementos distintos em valor absoluto**

- **INPUT:** Um vetor `A[1..n]` de inteiros, com `n ≥ 2`  
- **OUTPUT:** `max_{1 ≤ i < j ≤ n} |A[i] - A[j]|`

Ordene **A** em ordem crescente usando **MERGESORT**.

```pseudo
Ordene A em ordem crescente usando MERGESORT
maiorDif ← |A[n] - A[1]|
retorne maiorDif
```

Justifique por que o valor retornado (|A[n] - A[1]| após ordenar) é de fato a maior diferença absoluta entre dois elementos do vetor. Analise o tempo de execução do procedimento (inclua custo da ordenação e do passo de seleção).

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: SomaDuplicada (duas chamadas, três laços)**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza:

- Duas chamadas recursivas:
  - `x = SomaDuplicada(A[1..m])`
  - `y = SomaDuplicada(A[m+1..n])`
- Três laços que percorrem `A` inteiramente (cada um executa Θ(n) operações).

Escreva a recorrência para `T(n)` (inclua a hipótese em que `m = ⌊n/2⌋`)

---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e um valor `n₀`.

**(a)**  
`15n^2 + 200n + 50` é `O(g(n))` para qual `g(n)`? Mostre a prova com constantes `c` e `n₀`.

**(b)**  
`50n^3 + 10n^2 - 7` é `Ω(g(n))` para qual `g(n)`? Mostre a prova com constantes `c` e `n₀`.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Considere dois algoritmos:
- Algoritmo A possui tempo de execução `O(n log n)`.
- Algoritmo B possui tempo de execução `O(n^2)`.

Pergunta: Em teoria, A é mais eficiente que B para entradas suficientemente grandes? Fundamente a resposta, explique o conceito de ponto de cruzamento (`n₀`) e discuta como constantes e custos ocultos podem afetar instâncias práticas (dê um exemplo numérico ilustrativo).

**(b)**  
Se `f(n) = Θ(g(n))` e `h(n) = O(g(n))`, é verdade que `f(n) - h(n) = Ω(g(n))`? Forneça uma prova ou um contraexemplo bem explicado.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Soma dos elementos ímpares de `A`

**Requisitos:**
- Caso base claramente definido.
- Divisão explícita em duas metades (usar `m = ⌊n/2⌋`).
- Combinação correta dos resultados parciais.
- Justificativa breve da corretude (por indução ou argumento de invariante).

**Exemplo de pseudocódigo sugerido:**

```pseudo
function SomaImpares(A[1..n]):
    if n = 0 then
        return 0
    if n = 1 then
        if A[1] mod 2 = 1 then return A[1] else return 0
    m ← ⌊n/2⌋
    s1 ← SomaImpares(A[1..m])
    s2 ← SomaImpares(A[m+1..n])
    return s1 + s2
```

Explique por que este algoritmo é correto e apresente sua análise de tempo (recorrência).

---

**Instruções para entrega:** responda todas as questões mostrando todos os passos e justificativas. Seja claro e conciso.
