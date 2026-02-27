    # Lista 7B - Variante 3

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Menor diferença entre elementos adjacentes após ordenar (variante com COUNTING SORT)**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
    - **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]| (assuma inteiros no intervalo [0, k])`

    ```pseudo
    Ordene A em ordem crescente usando COUNTING-SORT (assuma inteiro em [0,k])
menorDif ← ∞
para i ← 1 até n-1 faça
    dif ← A[i+1] - A[i]
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

    **Algoritmo 2: Quadruplicar (quatro recursões)**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** Quatro chamadas recursivas sobre subvetores de tamanho ⌊n/2⌋ cada, laço n

    **Recorrência esperada:** `T(n) = 4 T(⌊n/2⌋) + Θ(n)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) 5n log n + 100 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) 5n^4 - n^2 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(n) vs B: O(n log n). Qual é mais eficiente?

    Explique que O(n) domina O(n log n) para grandes n e comente custos ocultos.

    **(b)**  
    (b) Se f=O(g) e h=O(g), então f+h = O(g)?

    Justifique sim e discuta quando Θ se aplica.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Número de elementos pares em A

    **Descrição adicional / restrições:** Divida A e some contagens de pares; caso base n=1 verifica A[1] par?1:0

