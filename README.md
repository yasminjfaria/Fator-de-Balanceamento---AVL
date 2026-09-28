# Inserção e Balanceamento da Árvore AVL

Nesta atividade, foram inseridos os seguintes valores na Árvore AVL:

**55, 26, 29, 13, 12, 11, 16, 1, 5, 29, -15, 4, 16, 8, 4, 5, 3, 1312, 100, 88.**

Durante as inserções, foi seguida a regra da Árvore Binária de Busca, em que os valores menores são posicionados à esquerda e os valores maiores à direita.

Para verificar se a árvore estava balanceada, foi analisada a altura das subárvores esquerda e direita de cada nó. A altura corresponde à quantidade de arestas existentes entre um nó e a folha mais distante abaixo dele.

O cálculo utilizado para verificar o balanceamento foi:

**FB = altura da esquerda - altura da direita**

Quando o resultado do Fator de Balanceamento (FB) está entre **-1 e +1**, o nó é considerado balanceado. Quando o resultado chega a **+2 ou -2**, é necessário realizar um balanceamento na árvore.

---

## Inserção do valor 29

Inicialmente, o valor **55** foi inserido e se tornou a raiz da árvore.

Em seguida, foi inserido o valor **26**. Como 26 é menor que 55, ele ficou à esquerda da raiz.

Ao inserir o valor **29**, foi realizada a seguinte comparação:

- 29 < 55, então seguimos para a esquerda;
- 29 > 26, então o valor foi inserido à direita do 26.

Depois dessa inserção, o nó 55 ficou desbalanceado.

### Cálculo

- Altura da esquerda = 1
- Altura da direita = -1

**FB(55) = 1 - (-1) = +2**

Como o valor foi inserido na direita do filho esquerdo, foi necessário realizar um balanceamento do tipo **Esquerda-Direita (LR)**.

Após o balanceamento, o valor **29** passou a ocupar a posição central entre os valores 26 e 55.

---

## Inserção do valor 12

Depois da inserção dos valores **13** e **12**, o nó 26 ficou com a subárvore esquerda maior que a direita.

### Cálculo

- Altura da esquerda = 1
- Altura da direita = -1

**FB(26) = 1 - (-1) = +2**

Como o crescimento ocorreu no lado esquerdo, foi necessário realizar o balanceamento dessa região.

Depois da correção, o valor **13** passou a ficar acima dos valores 12 e 26.

---

## Inserção do valor 11

Ao inserir o valor **11**, ocorreu um novo desbalanceamento, dessa vez no nó 29.

### Cálculo

- Altura da esquerda = 2
- Altura da direita = 0

**FB(29) = 2 - 0 = +2**

Como o resultado foi +2, foi necessário realizar novamente o balanceamento da árvore.

Após o balanceamento, o valor **13** passou a ocupar uma posição superior nessa região.

---

## Inserção do valor 1

O valor **1** foi inserido à esquerda do valor 11.

Após essa inserção, o nó 12 ficou desbalanceado.

### Cálculo

- Altura da esquerda = 1
- Altura da direita = -1

**FB(12) = 1 - (-1) = +2**

Foi realizado o balanceamento e, após a correção, o valor **11** passou a ficar entre os valores 1 e 12.

---

## Inserção do valor 4

Após as inserções dos valores **5, 29, -15 e 4**, ocorreu um novo desbalanceamento na região do nó 11.

### Cálculo

- Altura da esquerda = 2
- Altura da direita = 0

**FB(11) = 2 - 0 = +2**

Nesse caso, o crescimento ocorreu na direita da subárvore esquerda. Por isso, foi necessário realizar um balanceamento do tipo **Esquerda-Direita (LR)**.

---

## Inserção da segunda ocorrência do valor 16

O valor **16** já estava presente na árvore, porém o visualizador utilizado permitiu inserir uma segunda ocorrência.

Após essa inserção, o nó 26 ficou desbalanceado.

### Cálculo

- Altura da esquerda = 1
- Altura da direita = -1

**FB(26) = 1 - (-1) = +2**

Foi necessário realizar o balanceamento dessa região para manter a estrutura da árvore organizada e balanceada.

---

## Inserção do valor 88

Depois da inserção dos valores **1312, 100 e 88**, ocorreu outro desbalanceamento.

O valor 88 ficou abaixo do valor 100, que estava abaixo do 1312.

No nó 1312, foi realizado o seguinte cálculo:

- Altura da esquerda = 1
- Altura da direita = -1

**FB(1312) = 1 - (-1) = +2**

Como o nó ficou desbalanceado, foi necessário realizar o balanceamento dessa parte da árvore.

Após a correção, o valor **100** passou a ficar entre os valores 88 e 1312.

---

# Resultado após as inserções

Depois de realizar todas as inserções e os balanceamentos necessários, a árvore permaneceu balanceada.

Neste ponto, foi utilizado o visualizador de Árvore AVL disponibilizado no material da disciplina para acompanhar as alterações realizadas na estrutura.

---

# Remoções

Depois da etapa de inserção, foram removidos os seguintes valores:

**4, 29, 100, 5, 15, 16 e 55.**

Durante as remoções, foram considerados os três casos estudados:

- remoção de nó folha;
- remoção de nó com um filho;
- remoção de nó com dois filhos.

---

## Remoção do valor 4

O primeiro valor **4** encontrado possuía dois filhos.

Para realizar a remoção, foi utilizado o valor imediatamente menor disponível nessa região da árvore.

O valor **3** foi utilizado para substituir o 4.

Depois da remoção, a árvore continuou balanceada e não foi necessário realizar uma nova rotação.

---

## Remoção do valor 29

O nó **29** também possuía dois filhos.

O maior valor disponível na sua subárvore esquerda era o **26**.

Dessa forma, o valor 26 foi utilizado para substituir o 29.

Após a remoção, a árvore continuou balanceada.

---

## Remoção do valor 100

O nó **100** possuía dois filhos: **88 e 1312**.

O valor imediatamente menor era o **88**.

Por esse motivo, o valor 88 passou a ocupar a posição que anteriormente pertencia ao 100.

Depois dessa operação, a árvore permaneceu balanceada.

Nos casos em que o nó possui dois filhos, pode ser utilizado o valor imediatamente maior ou o valor imediatamente menor, dependendo da implementação utilizada.

---

## Remoção do valor 5

O primeiro valor **5** encontrado também possuía dois filhos.

Para realizar a remoção, foi utilizado o valor **4** para substituí-lo.

Por esse motivo, na árvore final, o lado esquerdo da raiz passou a apresentar o valor 4 nessa posição.

---

## Remoção do valor 15

Ao realizar a busca pelo valor **15**, ele não foi encontrado na árvore.

Por isso, nenhuma alteração foi realizada nessa etapa.

---

## Remoção do valor 16

Existiam duas ocorrências do valor **16** na árvore.

Ao remover uma delas, a outra permaneceu.

Depois dessa remoção, ocorreu um desbalanceamento na região do nó 26.

### Cálculo

- Altura da esquerda = 0
- Altura da direita = 2

**FB(26) = 0 - 2 = -2**

Como o resultado foi -2, o nó ficou desbalanceado para o lado direito.

Por isso, foi necessário realizar o balanceamento dessa região.

---

## Remoção do valor 55

O valor **55** possuía dois filhos.

Para realizar a remoção, foi utilizado o maior valor existente na sua subárvore esquerda, que era o **29**.

Assim, o valor 29 passou a ocupar a posição do 55 e a ocorrência utilizada na substituição foi removida.

Depois dessa operação, não foi necessário realizar outro balanceamento.

---

# Árvore final

Depois de realizar todas as inserções, balanceamentos e remoções, foi obtida a árvore final.

Os valores **4, 29, 5 e 16** ainda aparecem na árvore porque existiam duas ocorrências de cada um deles na sequência original de inserção, enquanto foi solicitada a remoção de apenas uma ocorrência.

O valor **15** não aparece porque ele não fazia parte da sequência de valores inseridos.

---

# Verificação do balanceamento final

Para confirmar que a árvore final continuou balanceada, foram realizados alguns cálculos do Fator de Balanceamento.

## Nó 13

A raiz da árvore possui o valor 13.

- Altura da subárvore esquerda = 3
- Altura da subárvore direita = 2

**FB(13) = 3 - 2 = +1**

Como o resultado é +1, o nó 13 está balanceado.

---

## Nó 4

- Altura da esquerda = 1
- Altura da direita = 2

**FB(4) = 1 - 2 = -1**

O nó 4 está balanceado.

---

## Nó 11

- Altura da esquerda = 1
- Altura da direita = 0

**FB(11) = 1 - 0 = +1**

O nó 11 está balanceado.

---

## Nó 29

- Altura da esquerda = 1
- Altura da direita = 1

**FB(29) = 1 - 1 = 0**

O nó 29 está balanceado.

---

## Nó 26

- Altura da esquerda = 0
- Altura da direita = -1

**FB(26) = 0 - (-1) = +1**

O nó 26 está balanceado.

---

## Nó 88

- Altura da esquerda = -1
- Altura da direita = 0

**FB(88) = -1 - 0 = -1**

O nó 88 também está balanceado.

Como todos os fatores de balanceamento analisados ficaram entre **-1 e +1**, foi possível verificar que a árvore final permaneceu balanceada.

---

# Conclusão

Nesta atividade foi possível acompanhar, na prática, o funcionamento de uma Árvore AVL desde a inserção dos elementos até a realização das remoções.

Durante as inserções, os valores foram organizados seguindo as regras de uma Árvore Binária de Busca, em que os valores menores ficam à esquerda e os maiores ficam à direita. Sempre que foi identificado algum desbalanceamento entre as subárvores, foi necessário realizar o balanceamento para manter a estrutura da árvore AVL.

Na etapa de remoção, foram analisadas diferentes situações, como nós com um filho e nós com dois filhos. Também foi possível observar o comportamento da árvore quando o valor procurado não existia, como aconteceu com o valor 15.

Depois de todas as inserções e remoções, foram verificados novamente os fatores de balanceamento de alguns nós. Os resultados permaneceram entre -1 e +1, indicando que a árvore final continuou balanceada e mantendo as propriedades de uma Árvore Binária de Busca.
