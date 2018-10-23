# Lista 2

## CSP

### **1.** Considere o problema de alocação de 𝑘 cavalos em um tabuleiro de xadrez 𝑛 × 𝑛 tal que nenhum cavalo é atacado. Assume-se que 𝑘 é dado e que 𝑘 ≤ 𝑛^2

#### a. Formule o problema CSP

D = {k | 1 ≤ k ≤ n^2}

X = {x, y | 0 ≤ x n, 0 ≤ y ≤ n}

C = {{x + 1, y + 2} = vazio, {x - 1, y + 2} = vazio}, {x + 1, y - 2} = vazio, {x - 1, y - 2} = vazio}

#### b. Considere agora o problema de colocar no tabuleiro tantos cavalos quanto for possível, sem que nenhum seja atacado. Explique como resolver esse problema usando uma busca local a partir da definição adequada da funções AÇÃO e RESULTADO e da função objetivo

### **2.** Dê uma formulação CSP precisa para o seguinte problema: Alocação de Disciplinas: Existe um número fixo de professores e de salas de aula, uma lista de disciplinas a serem oferecidas e uma lista de possíveis horários para as disciplinas. Cada professor tem um conjunto de disciplinas que ele(a) pode lecionar

X = {professores}

D = {cada professor possui uma lista de disciplinas que lecionará}

C = {para cada lista disciplina de um professor, não pode haver disciplinas no mesmo horário, e elas devem ser distribuídas aos professores igualmente}

### **3.** Mostre como uma única restrição ternária do tipo 𝐴 + 𝐵 = 𝐶 pode se tornar três restrições binárias através do uso de uma variável auxiliar. Você pode assumir domínios finitos (Dica: Considere uma nova variável que recebe valores que são pares de outros valores, e considere restrições do tipo “X é o primeiro elemento do par Y”). Em seguida, mostre como restrições com mais do que três variáveis podem ser tratadas de forma similar. Finalmente, mostre como restrições unárias podem ser eliminadas pela alteração do domínio das variáveis. Isto completa a demonstração de que qualquer CSP pode ser transformado em um CSP com apenas restrições binárias

Introduzimos uma nova variável AB. Se o domínio de A e B é o conjunto de números N, então o domínio de AB é o conjunto de pares de número de N, N x N.

Então, dizemos que existem três restrições binárias: o valor de A deve ser igual ao primeiro elemento do par AB, o valor de B deve ser igual ao segundo elemento do par AB, e a soma de pares AB deve ser igual a C.

Para restrições com mais de três variáveis, por exemplos A, B, C e D, podemos reduzir primeiro A, B e C exatamente como demonstrado, e depois adicionar D numa restrição ternaria com AB e C, e depois reduzir esta restrição ternaria numa restrição binaria introduzindo a variável CD.

### **4.** Considere o seguinte quebra-cabeça: Em uma mesma rua, há cinco casas de diferentes cores. Em cada uma delas, vive uma pessoa de uma nacionalidade diferente. Cada uma dessas pessoas gosta de uma bebida diferente e de uma marca de doces diferente da dos demais. Além disso, cada uma possui uma espécie diferente de animal de estimação. As perguntas são: Onde a zebra mora e em qual casa se bebe água?

**Pistas:**

* O britânico mora na casa vermelha.
* O espanhol possui um cão.
* O norueguês vive na primeira casa à esquerda.
* A casa verde está imediatamente à direita da casa de marfim.
* O homem que come barras de ‘Hershey’ mora na casa ao lado do homem com a raposa.
* ‘Kit Kats’ são comidos na casa amarela.
* O norueguês mora ao lado da casa azul.
* O comedor de ‘Smarties’ tem caracóis de estimação.
* O comedor ‘Snickers’ bebe suco de laranja.
* O ucraniano bebe chá.
* Os japoneses comem ‘Milky Ways’.
* ‘Kit Kats’ são comidos em uma casa ao lado da casa onde o cavalo é mantido.
* O café é bebido na casa verde.
* Leite é bebido na casa do meio.

#### Faça uma representação desse problema como um CSP e tente implementá-lo

```
X = {
    casas: {vermelha, azul, amarela, verde, marfim},
    doces: {kit kat, smarties, snickers, milky ways, hershey}
    bebidas: {suco de laranja, café, leite, chá, *água}
    pessoas: {britânico, espanhol, norueguês, japones, ucraniano}
    animais: {cavalo, cão, raposa, caracol, *zebra}
};

D de i = {casa, pessoa, bebida, doce, animal  para cada i};

C = [
  {
    pessoa: norueguês
    posição: 1
  },
  {
    casa: azul
    posição: 2
  },
  {
    bebida: leite
  },
  {

  },
  {

  },
]
```

### **9.** Defina com suas próprias palavras os termos: restrição, busca backtracking e consistência de arco

* **Restrição:** condição que não pode acontecer para a sua solução ser válida. Por exemplo, se a restrição é que A <> 2 em um conjunto X, A nunca pode ser 2.
* **Busca backtracking:** tipo de busca em profundidade, que salva o valor de cada nó em apenas uma variável, não atribui valores conflitantes com restrições e para de expandir um nó ao atingir uma solução infactível.
* **Consistência de arco:** para um arco entre A e B, ele é dito consistente caso para todo valor no domínio de A, existe um valor consistente em B, ou seja, que não infrinja nenhuma restrição.

## Competição

### **1.** Formalize e implemente um jogo (descrições de estado, ações, resultado de transição de estado, estado terminal e função utilidade) para um ou mais dos seguintes jogos estocásticos: jogo imobiliário (ou monopoly), scrabble, Texas hold’em poker

#### Jogo imobiliário

* **S0:** 
* **Jogador(s):** 
* **Acoes(s):** 
* **Result(s, a):** 
* **Terminal(s):** 
* **Utilidade:** 