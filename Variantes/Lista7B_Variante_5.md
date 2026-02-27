# Lista 7B - Variante 5

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre valores reais (vetor de doubles)**

- **INPUT:** Um vetor `A[1..n]` de números reais distintos, com `n ≥ 2`  
- **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|`, onde os valores de A são reais distintos

Ordene **A** em ordem crescente usando **MERGESORT** (comparações em ponto flutuante).

```pseudo
Ordene A usando MERGESORT
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

**Algoritmo 2: Recorrência com custo quadrático**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza duas chamadas recursivas (cada uma sobre metade do vetor) e faz trabalho adicional Θ(n²) por nível devido a laços aninhados que percorrem o vetor.


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e um valor `n₀`.

**(a)**  
`100 n + 1000` é `O(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `100 n + 1000 = O(g(n))`.

**(b)**  
`n` é `Ω(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `n = Ω(g(n))`.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Considere dois algoritmos:

- Algoritmo A possui tempo de execução `O(2^n)`.
- Algoritmo B possui tempo de execução `O(n!)`.

Pergunta: Qual é "melhor" (mais eficiente) assintoticamente? Explique as classes exponencial e factorial, comparando taxas de crescimento (por exemplo, n! cresce mais rápido que 2^n) e discuta implicações práticas.

**(b)**  
Se `f = O(g)` e `h = Ω(g)`, é verdade que `f·h = Θ(g^2)`? Forneça um contraexemplo rigoroso mostrando que a afirmação não é necessariamente verdadeira.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Máximo elemento par em A (retornar `-∞` se não existir)

**Descrição adicional / restrições:** Divida `A` em duas metades; para cada metade recursivamente obtenha o máximo par (ou `-∞` se não existir) e combine retornando `max(max_esq, max_dir)`.

Exemplo de pseudocódigo:

```pseudo
function MaximoPar(A[1..n]):
    if n = 0 then
        return -∞
    if n = 1 then
        if A[1] mod 2 = 0 then return A[1] else return -∞
    m ← ⌊n/2⌋
    lmax ← MaximoPar(A[1..m])
    rmax ← MaximoPar(A[m+1..n])
    return max(lmax, rmax)
```

Justifique por indução que a combinação devolve o máximo par global e escreva a recorrência para o tempo de execução do algoritmo.

---

