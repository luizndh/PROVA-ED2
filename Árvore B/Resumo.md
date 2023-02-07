# Introdução

1. Foi criada para resolver o problema de quando nossa estrutura de dados não cabe inteiramente na memória principal.
2. Ela não é uma árvore binária, ou seja, cada nó pode ter mais do que 2 filhos.
3. Cada nó também recebe o nome de página, e cada página pode ter várias chaves e ponteiros. 
4. Cada página da árvore tem que estar pelo menos 50% ocupada, tirando a raíz, para que a estrutura seja eficiente.
5. Não pode haver uma chave sem filho em uma página.
6. Todas as folhas da árvore estão sempre no mesmo nível, pois a árvore cresce para cima e não para baixo.

## Ordem da árvore

De acordo com Cormen, Bayer e McCreight, a ordem de uma árvore seria a quantidade de chaves que uma página pode ter dividido por 2.

De acordo com Knuth, a ordem da árvore seria o número de ponteiros de cada página, ou seja, a quantidade de filhos que um nó pode ter. Também é a quantidade de chaves 
de uma página + 1.

## Busca

Funciona igual a uma árvore binária de busca, porém todas as chaves de uma página são verificadas até que o número desejado seja uma das chaves ou esteja em um intervalo entre elas.

## Inserção

Procura o lugar igual uma árvore binária de busca. Se há espaço na página, apenas adicione a chave no lugar correto e pronto. Se a página estiver cheia, faça o seguinte:
1. Divide a página em dois
2. Deixe a primeira metade das chaves na página inicial, e coloque a outra metade na nova página criada
3. Insira o novo número na página ideal
4. Caso o elemento tenha sido inserido na página inicial, o último elemento dessa página deve ser promovido. Caso tenha sido inserido na nova página criada, o primeiro dela sobe.
5. Caso a página de cima esteja cheia, repita o processo todo

## Remoção
