# Estrutura de dados 

### Dispositivos de memória do computador: 
- <strong>ROM:</strong> Read Only Memory
- <strong>RAM:</strong> Random Acess Memory <br>
  Dispositivo de armazenamento eletrônico que suporta a leitura e a escrita de dados. É uma estrutura tridimensional (grade,linha e coluna) 
  de unidade de armazenamento e possui um acesso rápido. 
  
  
  ### Alocação de memória
  
  - <strong>Estática:</strong> Feita de forma prévia (Variáveis globais ou estáticas), gera unidades dememória ociosas.
  - <strong>Dinâmica:</strong> É realizada conforme a demanda, assim, um ponteiro faz referência a um endereço de memória, já que os dados ficam dispersos na memória.

  <h4> Programa -> Algoritmo -> Linguagem de programação -> Compilação -> Código de máquina -> Processador</h4>

  ### Fila estática: 
   - Pode ser implementada em um arranjo unidimensional;
   - Regra: <strong>FIFO (First in First Out) ou o primeiro que entra é o primeiro que sai</strong>;
   - Dois pontos de acesso (Head e tail);
   - Operações de enqueue e dequeue;
   - Algoritmo de inserção:
    ```
    // Verifica se a fila está cheia antes de inserir
    IsFull(V)
      se tail = |V|
        retorna verdadeiro
      senão
        retorna false

    // Enqueue

    Enqueue(V,x)
      se !IsFull(V)
        V[tail] <- x
        tail <- tail+1
      senão
        erro overflow
    ```
     1. A variável recebe um valora ser adicionado;
     2. Verifica se a fila está cheia;
     3. Adiciona o número.
     4. A operação de dequeue faz o contrário,utilizando a head do vetor.


  ### Pilha estática:
    - Arranjo unidimensional;
    - Um único ponto de acesso (Topo);
    - <strong> LIFO (Last in First Out) ou o último que entra é o primeiro que sai.</strong>
    - Operações push (inserção) e pop (retirada).
    - Algoritmos:
      ```
      Push (x,V)
        se !IsFull(V)
          V[topo] <- x
          topo <- topo + 1
        senão erro overflow


      Pop(x, V) 
        se !IsEmpty(V)
          x <- V[topo]
          topo <- topo - 1
          retorna x
        senão
          erro underflow
      ```
