    # Lista 7B - Variante 6

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Menor diferença considerando índices distintos e valores repetidos permitidos**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros distintos, com `n ≥ 2`  
    - **OUTPUT:** `min_{i ≠ j} |A[i] - A[j]| (valores não necessariamente distintos)`

    ```pseudo
    Ordene A usando MERGESORT
verifique adjacentes; se houver iguais, menorDif = 0
caso contrário, igual ao caso distinto
    ```

    ---

    ## Q2

    Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
    (Não é preciso resolver nem justificar.)

    **Algoritmo 2: Recorrência com custo logarítmico**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** duas chamadas e laço de tamanho log n

    **Recorrência esperada:** `T(n) = 2 T(⌊n/2⌋) + Θ(log n)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) 2^{n} + n^5 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) 2^n é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(n^1.5) vs B: O(n log n). Compare: qual cresce mais rápido?

    Discuta que n^1.5 grows faster than n log n for large n.

    **(b)**  
    (b) Se f=Θ(g) e h=Θ(g), então (f+h)/2 = Θ(g)?

    Mostre que sim.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Σ A[i]^2 tal que A[i] é par

    **Descrição adicional / restrições:** Divida e some quadrados onde aplicável

