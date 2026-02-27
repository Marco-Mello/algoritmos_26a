# Lista 7B - Variante 4

**Nome:**

---

## Q1

Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

**Algoritmo 1: Menor diferença entre dois elementos distintos (sem ordenar explicitamente)**

- **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
- **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|`

```pseudo
Use uma tabela de hash para inserir e procurar vizinhos ±1, ±2,... até encontrar menor diferença (descrição informal)
```

---

## Q2

Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
(Não é preciso resolver nem justificar.)

**Algoritmo 2: Soma com recursão desigual**

- **INPUT:** Um vetor `A[1...n]`

(Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)


---

## Q3

Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

**(a)**  
(a) 7n^3 - n é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

**(b)**  
(b) n^2 log n é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

---

## Q4

Responda cada item e justifique formalmente.

**(a)**  
(a) A: O(n^2) vs B: O(n^2) com constantes diferentes

Discuta que assintoticamente iguais, mas constantes e memória importam.

**(b)**  
(b) Se f=Ω(g) e h=Ω(g), então f+h = Ω(g)?

Justifique afirmativa.

---

## Q5

Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

- **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
- **OUTPUT:** Soma de A[i] para i par

**Descrição adicional / restrições:** Divida e combine somas de posições pares (ajustar índices na metade direita)

