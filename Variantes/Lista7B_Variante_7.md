# Lista 7B - Variante 7

**Nome:** __________________________

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **Θ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença em conjunto circular (considerar diferença circular)**

- **INPUT:** Um vetor `A[1..n]` de inteiros, com `n ≥ 2`  
- **OUTPUT:** menor diferença circular entre os valores (isto é, considere os valores ordenados em círculo e calcule a menor |A[i] - A[j]| levando em conta a circularidade)

Ordene **A** via **MERGESORT** e calcule as diferenças entre adjacentes; inclua também a diferença entre o último e o primeiro elemento (`|A[n] - A[1]|`) ao tomar o mínimo.

```pseudo
Ordene A usando MERGESORT
menorDif ← |A[2] - A[1]|
para i ← 2 até n-1 faça
    menorDif ← min(menorDif, |A[i+1] - A[i]|)
fim para
menorDif ← min(menorDif, |A[n] - A[1]|)
retorne menorDif
```

Justifique por que basta verificar diferenças entre adjacentes e também entre `A[n]` e `A[1]` para obter a menor diferença no sentido circular. Apresente a análise de complexidade temporal (inclua custo da ordenação).

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Recorrência com três chamadas e laço n log n**

- **INPUT:** Um vetor `A[1..n]`

O algoritmo realiza três chamadas recursivas (cada uma sobre um subvetor de tamanho ⌊n/2⌋) e trabalho adicional Θ(n log n) por nível.


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove formalmente, indicando constantes positivas e um valor `n₀`.

**(a)**  
`n^2 log n + 50 n^2` é `O(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `n^2 log n + 50 n^2 = O(g(n))`.

**(b)**  
`n^3 + n^2` é `Ω(g(n))` para qual `g(n)`? Prove com constantes `c` e `n₀` que `n^3 + n^2 = Ω(g(n))`.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
Considere dois algoritmos:
- Algoritmo A possui tempo de execução `O(log n)`.
- Algoritmo B possui tempo de execução `O(1)`.

Pergunta: qual é melhor? Explique por que `O(1)` é assintoticamente melhor que `O(log n)`, mas discuta situações práticas (por exemplo, quando `O(1)` pode ter constantes mais altas ou quando acesso a memória/cache faz diferença).

**(b)**  
Se `f = O(g)` e `h = o(g)`, então `f + h = O(g)`? Prove formalmente e explique por que a soma de um termo Big-O com um termo little-o permanece Big-O do mesmo g.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos, e um parâmetro inteiro `K`
- **OUTPUT:** Soma dos elementos pares menores que `K`

**Descrição adicional / restrições:** Divida `A` em duas metades; recursivamente calcule a soma restrita em cada metade; na combinação, some apenas valores menores que `K`.

Exemplo de pseudocódigo:

```pseudo
function SomaParesMenoresK(A[1..n], K):
    if n = 0 then
        return 0
    if n = 1 then
        if A[1] mod 2 = 0 and A[1] < K then return A[1] else return 0
    m ← ⌊n/2⌋
    s1 ← SomaParesMenoresK(A[1..m], K)
    s2 ← SomaParesMenoresK(A[m+1..n], K)
    return s1 + s2
```


---

**Instruções para entrega:** responda todas as questões mostrando todos os passos e justificativas. Seja claro e conciso.
