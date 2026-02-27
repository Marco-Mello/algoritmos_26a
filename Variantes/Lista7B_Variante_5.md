    # Lista 7B - Variante 5

    **Nome:**

    ---

    ## Q1

    Analise o algoritmo a seguir. Justifique formalmente sua corretude (explique por que o algoritmo resolve corretamente o problema proposto) e analise o tempo de execução.  
    A sua resposta deve estar em **ϴ**, se possível. Caso não seja possível, utilize notação **O** com uma análise justa (sem folga) para o pior caso.

    **Algoritmo 1: Menor diferença entre valores reais (vetor de doubles)**

    - **INPUT:** Um vetor `A[1...n]` de n inteiros distintos, com `n ≥ 2`  
    - **OUTPUT:** `min_{1 ≤ i < j ≤ n} |A[i] - A[j]|, A contém reais distintos`

    ```pseudo
    Ordene A em ordem crescente usando MERGESORT (com comparação de reais)
calcule menorDif entre adjacentes como no algoritmo original
    ```

    ---

    ## Q2

    Escreva uma **recorrência** para o tempo de execução do algoritmo a seguir.  
    (Não é preciso resolver nem justificar.)

    **Algoritmo 2: Recorrência com custo quadrático**

    - **INPUT:** Um vetor `A[1...n]`

    (Descreva a recorrência para o tempo de execução do algoritmo que executa as chamadas recursivas e tem o custo descrito abaixo)

    **Custo descrito:** duas chamadas e laços aninhados O(n²)

    **Recorrência esperada:** `T(n) = 2 T(⌊n/2⌋) + Θ(n²)`

    ---

    ## Q3

    Escolha, para cada item, a função que corresponde ao valor assintótico **(justo, sem folga)** e prove.

    **(a)**  
    (a) 100n + 1000 é `O(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    **(b)**  
    (b) n é `Ω(g(n))` para qual `g(n)`? Explique e prove com constantes e n0.

    ---

    ## Q4

    Responda cada item e justifique formalmente.

    **(a)**  
    (a) A: O(2^n) vs B: O(n!). Quem é melhor?

    Explique classes exponencial vs factorial

    **(b)**  
    (b) Se f=O(g) e h=Ω(g), então f·h = Θ(g^2)?

    Mostre que não necessariamente, dê contraexemplo.

    ---

    ## Q5

    Escreva um algoritmo de **divisão e conquista** para o seguinte problema.  
    Escreva pseudocódigo detalhado e justifique brevemente sua corretude.  
    O algoritmo deve dividir o vetor em duas partes em cada chamada recursiva.

    - **INPUT:** Um vetor `A[1..n]` de inteiros não-negativos  
    - **OUTPUT:** Máximo elemento par em A (retornar -∞ se não existir)

    **Descrição adicional / restrições:** Divida A; combine retornando max entre maxes da esquerda e direita

