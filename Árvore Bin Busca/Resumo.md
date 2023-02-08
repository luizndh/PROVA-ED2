## Árvore Binária de Busca
Uma árvore binária de busca é uma estrutura de dados em que cada nó tem no máximo dois filhos, e todos os valores da sub árvore esquerda possuem valores menores que a raiz e os da direita possuem valores maiores que a raiz.

## Complexidade
- Busca, inserção e exclusão: O(log N)

## Operações

### Inserção
Começando pela raiz, se o valor a ser inserido for menor que o nó atual, avançamos para a subárvore esquerda, caso contrário, avançamos para a subárvore direita. Esse processo se repete até encontrar um nó nulo, onde o elemento é inserido.

### Busca
Começando pela raiz, comparamos o valor do elemento a ser buscado com o valor do nó atual. Se o valor for igual, encontramos o elemento desejado. Caso não seja, avançamos para a subárvore esquerda ou direita, dependendo se o valor é menor ou maior do que o nó atual.

### Exclusão
