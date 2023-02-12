## Árvore Rubro-Negra
Uma árvore Rubro-Negra é uma estrutura de dados balanceada, baseada em uma árvore binária. Essa estrutura tem as seguintes regras:
-Cada nó é vermelho ou preto
-A raiz e as folhas NIL são pretas
-Um nó vermelho só tem filhos pretos
-Todos os caminhos de um nó até as folhas contêm o mesmo número de nós pretos.

## Complexidade
- Busca, inserção e exclusão: O(log N)

## Rotações

### Esquerda:
O filho direito do nó rotacionado o substitui, e o nó rotacionado vira o filho esquerdo do filho direito. A sub árvore esquerda do filho direito do nó rotacionado vira a sub árvore direita do nó rotacionado.

Ou seja:
1- Substitua o nó rotacionado pelo seu filho à direita.
2- O filho à esquerda do filho à direita do nó rotacionado vira o filho à direita do nó rotacionado.

Exemplo:
![esquerda](https://user-images.githubusercontent.com/62142509/218327671-7c296fc9-977f-4c75-8bcc-d4b1ecabdc9d.png)

### Direita:
O filho esquerdo do nó rotacionado o substitui, e o nó rotacionado vira o filho direito do filho esquerdo. A sub árvore direita do filho esquerdo do nó rotacionado vira a sub árvore esquerda do nó rotacionado.

Ou seja:
1- Substitua o nó rotacionado pelo seu filho à esquerda.
2- O filho à direita do filho à esquerda do nó rotacionado vira o filho à esquerda do nó rotacionado.

## Operações

### Inserção

### Exclusão

### Busca
