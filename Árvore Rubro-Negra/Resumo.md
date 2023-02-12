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
1. Substitua o nó rotacionado pelo seu filho à direita.
2. O filho à esquerda do filho à direita do nó rotacionado vira o filho à direita do nó rotacionado.

Exemplo:
![esquerda](https://user-images.githubusercontent.com/62142509/218327719-76102692-83b9-491e-9434-112ff5d0547f.png)

### Direita:
O filho esquerdo do nó rotacionado o substitui, e o nó rotacionado vira o filho direito do filho esquerdo. A sub árvore direita do filho esquerdo do nó rotacionado vira a sub árvore esquerda do nó rotacionado.

Ou seja:
1. Substitua o nó rotacionado pelo seu filho à esquerda.
2. O filho à direita do filho à esquerda do nó rotacionado vira o filho à esquerda do nó rotacionado.

## Operações

### Inserção
1. O nó inserido será colorido vermelho.
2. Inserimos na árvore. Caso haja uma violação de propriedades, temos então 4 casos:
  1. Se o nó é raiz, será recolorido para preto.
  2. Se o tio do nó é vermelho, recolorimos o pai, avô e tio.
  3. Se o tio do nó é preto, e está em uma relação triângulo, rotacionamos o pai do nó, na direção contrária do nó.
  4. Se o tio do nó é preto, e está em uma relação de linha, rotacionamos o avô do nó, na direção contraria do nó. Depois disso, recolorimos os nós que eram o pai e o avô antes da rotação.
  Relação triângulo:
  ![triangulo](https://user-images.githubusercontent.com/62142509/218329048-974b7bbb-4afd-424c-99f0-c46aad071421.png)
  Relação linha:
  ![linha](https://user-images.githubusercontent.com/62142509/218329197-386e423c-ec2d-42d5-87fd-79cc2edf884a.png)

### Exclusão

### Busca
