    # Lista 7B - Variante 2

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Maior diferença entre dois elementos distintos em valor absoluto**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
    - **OUTPUT:** `max_{1 ≤ i < j ≤ n} |A[i] - A[j]|`

    ```pseudo
    Ordene A em ordem crescente usando MERGESORT
maiorDif ← |A[n] - A[1]|
retorne maiorDif
    ```

    ---

    ## Q2

    Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
    (Não é preciso resolver nem justificar.)

    **Algoritmo 2: SomaDuplicada (duas chamadas, três laços)**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** Duas chamadas recursivas e três laços de n

    **Recorrência esperada:** `T(n) = 2 T(⌊n/2⌋) + Θ(n)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) 15n^2 + 200n + 50 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) 50n^3 + 10n^2 - 7 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(n log n) vs B: O(n^2). Pergunta sobre eficiência teórica.

    Responder afirmando A é melhor assintoticamente e discutir crossover n0.

    **(b)**  
    (b) Se f=Θ(g) e h=O(g), é verdade que f-h = Ω(g)?

    Explique com exemplos quando é verdadeiro ou falso.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Soma dos elementos ímpares de A

    **Descrição adicional / restrições:** Divida A em duas metades; recursivamente calcule soma ímpares e some

