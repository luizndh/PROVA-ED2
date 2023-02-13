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

Exemplo:

![image](https://user-images.githubusercontent.com/79621478/218585439-66cb3c67-1906-4ee2-ab73-5defb5b4b8bf.png)


## Remoção

A remoção na árvore B possui basicamente 4 casos:

Caso 1 - Se o elemento estiver em uma folha e a folha mantiver 50% da ocupação após a remoção, basta remover e pronto.

Caso 2 - Caso o elemento não esteja em uma folha, basta trocá-lo pelo seu antecessor. Ao remover o antecessor, se a página em que ele estava ainda tiver 50% de ocupação ou mais, basta remover e pronto. 

Caso 3 - Caso em que a folha em que o elemento é removido, porém ela fica com menos do que 50% de ocupação. Nesse caso, veja a possibilidade de uma de suas irmãs cederem uma chave para ela, de forma que a chave cedida sobe para o seu pai, para ocupar o espaço da chave que será cedida para sua irmã.

Exemplo: 

![image](https://user-images.githubusercontent.com/79621478/218586308-5c84af0d-7f42-4c59-8615-28371a046d91.png)


Caso 4 - Caso em que a folha em que o elemento é removido, porém ela fica com menos do que 50% de ocupação e suas irmãs não podem ceder nenhuma chave. Nesse caso, fazemos uma fusão de folhas, juntando a página cujo elemento deve ser removido com uma de suas duas irmãs, e descendo uma das chaves do seu pai para completar a página. Caso o pai dessas irmãs fique com menos de 50% de ocupação, repita o processo.

![image](https://user-images.githubusercontent.com/79621478/218586990-92cc5c3c-ba0e-4110-978e-8dcc05704645.png)

