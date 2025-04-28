# 21. Merge Two Sorted Lists

Esta solução resolve o problema de mesclar duas listas ligadas ordenadas (list1 e list2) em uma nova lista também ordenada. A abordagem utilizada é *recursiva*.

## A lógica

Se uma das listas estiver vazia, retornamos a outra lista, pois ela já está ordenada.

Comparando os valores dos nós atuais de list1 e list2:

Se o valor de list1 for menor, list1 será o primeiro nó da lista resultante. Em seguida, chamamos a função recursivamente para mesclar list1.next e list2.

Caso contrário, list2 será o primeiro nó da lista resultante. Em seguida, chamamos a função recursivamente para mesclar list1 e list2.next.

A cada chamada recursiva, conectamos o nó menor ao próximo nó retornado pela fusão, construindo a lista ordenada progressivamente.

A recursão avança até que pelo menos uma das listas esteja vazia, momento em que simplesmente conectamos o restante da lista não vazia.

Essa abordagem garante que todos os nós sejam comparados e conectados de maneira ordenada, com complexidade $\mathcal{O}(n+m)$, onde n e m são os tamanhos das listas de entrada.