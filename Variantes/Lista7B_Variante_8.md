# Lista 7B - Variante 8

**Nome:**

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre elementos de duas metades (após particionar)**

- **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
- **OUTPUT:** `min de |A[i]-A[j]| onde i na metade esquerda e j na metade direita (variante)`

```pseudo
Particione A em duas metades; ordene cada metade e verifique pares na fronteira e internamente (descrição)
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Recorrência com uma chamada e custo linear**

- **INPUT:** Um vetor `A[1...n]`

(Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

**(a)**  
(a) n^3 + 100n^2 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

**(b)**  
(b) 10n^5 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
(a) A: O(n^3) vs B: O(n^2). Bob afirma A mais eficiente — avaliar.

Explique porque B é melhor (contrário da afirmação de Bob)

**(b)**  
(b) Se f=O(g) e h=Ω(g), é verdade que f+h = Θ(g)?


---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Soma de A[i] para i ímpar

**Descrição adicional / restrições:** Divida e combine com cuidado de índices

