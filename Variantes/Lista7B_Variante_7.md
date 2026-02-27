    # Lista 7B - Variante 7

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Menor diferença em conjunto circular (considerar diferença circular)**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
    - **OUTPUT:** `min diferença circular entre valores ordenados em círculo (|A[i] - A[j]| min circular)`

    ```pseudo
    Ordene A via MERGESORT
calcule diferenças entre adjacentes e também |A[n]-A[1]| e tome mínimo
    ```

    ---

    ## Q2

    Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
    (Não é preciso resolver nem justificar.)

    **Algoritmo 2: Recorrência com três chamadas e laço n log n**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** três chamadas e custo Θ(n log n)

    **Recorrência esperada:** `T(n) = 3 T(⌊n/2⌋) + Θ(n log n)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) n^2 log n + 50n^2 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) n^3 + n^2 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(log n) vs B: O(1). Quem é melhor?

    Explique que O(1) é melhor, mas hardware e implementação podem afetar.

    **(b)**  
    (b) Se f=O(g) e h=o(g), então f+h = O(g)?

    Mostre que sim.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Soma de elementos pares menores que K

    **Descrição adicional / restrições:** Divida; no combine, some somente valores < K (K parâmetro)

