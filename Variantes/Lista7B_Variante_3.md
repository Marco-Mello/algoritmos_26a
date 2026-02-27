# Lista 7B - Variante 3

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre elementos adjacentes após ordenar (variante com COUNTING-SORT)**

- **INPUT:** Um vetor `A[1..n]` de inteiros, com `n ≥ 2` (assuma `A[i] ∈ [0..k]` para algum inteiro `k`)
- **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|` (diferença mínima absoluta entre quaisquer dois elementos)

Ordene **A** em ordem crescente usando **COUNTING-SORT** (aplicável porque os elementos pertencem a `[0..k]`).

```pseudo
Ordene A usando COUNTING-SORT
menorDif ← ∞
para i ← 1 até n-1 faça
    dif ← A[i+1] - A[i]
    se dif < menorDif então
        menorDif ← dif
    fim se
fim para
retorne menorDif
```

Justifique por que olhar apenas diferenças entre elementos adjacentes após ordenar é suficiente para obter a diferença mínima entre quaisquer pares. Indique também a complexidade temporal do algoritmo em termos de `n` e `k` (use Θ quando possível).

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Quadruplicar (quatro recursões)**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza quatro chamadas recursivas, cada uma sobre um subvetor de tamanho `⌊n/2⌋`, e faz trabalho adicional Θ(n) (um laço que percorre o vetor):

- `x1 = Algo(A[1..⌊n/2⌋])`
- `x2 = Algo(A[⌊n/2⌋+1..n])`
- `x3 = Algo(A[1..⌊n/2⌋])`
- `x4 = Algo(A[⌊n/2⌋+1..n])`
- custo extra no nível: Θ(n)


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e um valor `n₀`.

**(a)**  
`5 n log n + 100` é `O(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `5 n log n + 100 = O(g(n))`.

**(b)**  
`5 n^4 - n^2` é `Ω(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `5 n^4 - n^2 = Ω(g(n))`.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Considere dois algoritmos:
- Algoritmo A possui tempo de execução `O(n)`.
- Algoritmo B possui tempo de execução `O(n log n)`.

Pergunta: qual é mais eficiente para entradas suficientemente grandes? Explique por que.

**(b)**  
Se `f(n) = O(g(n))` e `h(n) = O(g(n))`, então `f(n) + h(n) = O(g(n))`? Prove formalmente; discuta sob quais condições a soma é `Θ(g(n))`.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos
- **OUTPUT:** Número de elementos pares em `A`

**Descrição adicional / restrições:** Divida `A` em duas metades; no caso base `n = 1` retorne `1` se `A[1]` for par, caso contrário `0`.

Exemplo de pseudocódigo:

```pseudo
function ContaPares(A[1..n]):
    if n = 0 then
        return 0
    if n = 1 then
        if A[1] mod 2 = 0 then return 1 else return 0
    m ← ⌊n/2⌋
    c1 ← ContaPares(A[1..m])
    c2 ← ContaPares(A[m+1..n])
    return c1 + c2
```

---
