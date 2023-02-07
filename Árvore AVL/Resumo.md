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
Essa rotação necessita de duas rotações simples, sendo a primeira à direita e a segunda à esquerda.

![image](https://user-images.githubusercontent.com/79621478/217351638-e29b8f7d-5879-451a-973f-ed3133740685.png)

# Dupla à direita
Essa rotação necessita de duas rotações simples, sendo a primeira à esquerda e a segunda à direita.

![image](https://user-images.githubusercontent.com/79621478/217352756-d250ce19-aed3-42f0-8277-bfe2263e2231.png)

## Como decidir as rotações?
-Calcular o fator de balanceamento = altura sub-árvore direita - altura sub-árvore esquerda
-Se o fator for maior que 1:
  -Se a sub-árvore da direita tem o fator menor que 0:
    -rotação dupla à esquerda
  -Se a sub-árvore da direita tem o fator maior que 0:
    -rotação simples à esquerda

-Se o fator for menor que -1:  
  -Se a sub-árvore da esquerda tem o fator maior que 0:    
    -rotação dupla à direita  
  -Se a sub-árbore da esquerda tem o fator menor que 0:    
    -rotação simples à direita
