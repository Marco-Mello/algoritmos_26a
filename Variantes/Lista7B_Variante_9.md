# Lista 7B - Variante 9

**Nome:**

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença com restrição |i-j| ≤ k (janela)**

- **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
- **OUTPUT:** `min_{|i-j| ≤ k} |A[i] - A[j]|`

```pseudo
Percorra A mantendo uma estrutura (ex.: multiset) com elementos da janela de tamanho k e atualize mínimo
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Recorrência com 3 chamadas e custo constante**

- **INPUT:** Um vetor `A[1...n]`

(Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

**Custo descrito:** três chamadas e custo Θ(1)

**Recorrência esperada:** `T(n) = 3 T(⌊n/2⌋) + Θ(1)`

---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

**(a)**  
(a) 20n^2 + 5n é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

**(b)**  
(b) n^2 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
(a) A: O(n) vs B: O(n). Ambos iguais: quando escolher entre eles?

Discuta constantes, estabilidade, memória.

**(b)**  
(b) Se f=Θ(g) e h=Ω(g), então f+h = Ω(g)?

Mostre que sim.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Soma pares considerando A circular (sem duplicar elementos)

**Descrição adicional / restrições:** Divida e combine normalmente — observe invariantes de fronteira

