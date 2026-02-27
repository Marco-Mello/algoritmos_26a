# Lista 7B - Variante 6

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença considerando índices distintos e valores repetidos permitidos**

- **INPUT:** Um vetor `A[1..n]` de inteiros, com `n ≥ 2` (valores podem repetir)
- **OUTPUT:** `min_{i ≠ j} |A[i] - A[j]|` (valores não necessariamente distintos)

Ordene **A** usando **MERGESORT** e verifique adjacentes; se houver elementos iguais, então `menorDif = 0`, caso contrário calcule o mínimo entre adjacentes como no caso de valores distintos.

```pseudo
Ordene A usando MERGESORT
se existe i tal que A[i] = A[i+1] então
    retorne 0
fim se
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

**Algoritmo 2: Recorrência com custo logarítmico**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza duas chamadas recursivas (cada uma sobre metade do vetor) e faz trabalho adicional Θ(log n) por nível (por exemplo, um laço de comprimento log n).


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e um valor `n₀`.

**(a)**  
`2^{n} + n^5` é `O(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `2^{n} + n^5 = O(g(n))`.

**(b)**  
`2^n` é `Ω(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `2^n = Ω(g(n))`.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Considere dois algoritmos:
- Algoritmo A possui tempo de execução `O(n^{1.5})`.
- Algoritmo B possui tempo de execução `O(n log n)`.

Pergunta: qual cresce mais rápido para n → ∞? Explique por que `n^{1.5}` cresce mais rápido que `n log n` (use limites ou desigualdades) e discuta implicações práticas.

**(b)**  
Se `f = Θ(g)` e `h = Θ(g)`, então `(f+h)/2 = Θ(g)`? Prove formalmente com constantes ou exemplifique a igualdade de ordens de grandeza.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos
- **OUTPUT:** Σ A[i]^2 tal que A[i] é par

**Descrição adicional / restrições:** Divida `A` em duas metades; recursivamente calcule soma dos quadrados dos pares em cada metade e combine somando os resultados.

Exemplo de pseudocódigo:

```pseudo
function SomaQuadradosPares(A[1..n]):
    if n = 0 then
        return 0
    if n = 1 then
        if A[1] mod 2 = 0 then return A[1]^2 else return 0
    m ← ⌊n/2⌋
    s1 ← SomaQuadradosPares(A[1..m])
    s2 ← SomaQuadradosPares(A[m+1..n])
    return s1 + s2
```


---

**Instruções para entrega:** responda todas as questões mostrando todos os passos e justificativas. Seja claro e conciso.
