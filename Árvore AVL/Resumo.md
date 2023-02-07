## Introdução e complexidade
A árvore AVL é uma árvore binária auto-balanceável, ou seja, conforme você insere e remove elementos nela, ela se auto-balanceia através de rotações. Isso faz 
com que a busca, inserção e remoção sempre tenham complexidade O(log n), pois o pior caso seria ter que percorrer a altura da árvore inteira.

O balanceamento acontece de acordo com o equilíbrio da árvore, que é medido subtraindo a altura da subárvore direita da subárvore esquerda de um nó. Todos 
os nós possuem um nível de balanceamento, e quando esse nível é diferente de -1, 0 ou 1, quer dizer que a árvore está desbalanceada, e será necessário fazer
uma rotação para balanceá-la.

## Rotações
Para corrigir o desbalanceamento, existem 4 tipos de rotações. Simples à direita e à esquerda, e dupla à esquerda e à direita.

# Simples à esquerda e à direita
Esquerda:

![image](https://user-images.githubusercontent.com/79621478/217350068-38e66a76-8c5d-4952-a8e4-a15a6c53dc76.png)

Direita:

![image](https://user-images.githubusercontent.com/79621478/217350630-ff9b667c-bb0b-43d7-8769-d7541249a55a.png)

# Dupla à esquerda
