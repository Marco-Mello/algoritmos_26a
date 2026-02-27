# Lista 7B - Variante 10

**Nome:**

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença em número grande de elementos; enfoque em complexidade prática**

- **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
- **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|, discuta trade-offs entre sorters e uso de seleção linear`

```pseudo
Ordene usando MERGESORT ou QUICKSORT de bom pivô; ou use aproximações se memória limitada
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Recorrência com 3 chamadas e custo n²**

- **INPUT:** Um vetor `A[1...n]`

(Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

**Custo descrito:** três chamadas e custo Θ(n²)


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

**(a)**  
(a) 3n log n + 10 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

**(b)**  
(b) 7n^3 + 3n log n é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
(a) A: O(n log n) vs B: O(n log n) com recursões diferentes

Discussão sobre implementações e overhead de recursão.

**(b)**  
(b) Se f=O(g) e h=Θ(g), é (f+h)/2 = Θ(g)?

Analise e exemplifique.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Soma dos elementos pares com ênfase em paralelismo na combinação

**Descrição adicional / restrições:** Divida em duas metades e combine; descreva speedup e custo

