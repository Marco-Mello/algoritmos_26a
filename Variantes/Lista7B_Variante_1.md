    # Lista 7B - Variante 1

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Menor diferença entre dois elementos distintos em valor absoluto**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros, com `n ≥ 2`  
    - **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|`

    ```pseudo
    Ordene A em ordem crescente usando MERGESORT
menorDif ← |A[2] - A[1]|

para i ← 2 até n-1 faça
    dif ← |A[i+1] - A[i]|
    se dif < menorDif então
        menorDif ← dif
    fim se
fim para
    ```

    ---

    ## Q2

    Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
    (Não é preciso resolver nem justificar.)

    **Algoritmo 2: TriplaSoma (original)**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** Três chamadas recursivas: x=TriplaSoma(1..m), y=TriplaSoma(m+1..n), z=TriplaSoma(1..m); laços 4×n

    **Recorrência esperada:** `T(n) = 3 T(⌊n/2⌋) + Θ(n)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) 10n^2 + 100n - 1 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) 20n^3 - 10n + 100 é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(n^2) vs B: O(n^3). Bob afirma A mais eficiente — avaliar.

    Explique por que A é teoricamente melhor no limite, mas discuta constantes e casos práticos.

    **(b)**  
    (b) Se f=O(g) e h=Ω(g), é verdade que (f+h)/2 = Θ(g)?

    Analise contrapexemplos e condições adicionais necessárias.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Soma dos elementos pares de A

    **Descrição adicional / restrições:** Divida A em duas metades, recursivamente calcule soma pares esquerda e direita; combine somando-os

