# Lista 2

## CSP

### **1.** Considere o problema de alocação de 𝑘 cavalos em um tabuleiro de xadrez 𝑛 × 𝑛 tal que nenhum cavalo é atacado. Assume-se que 𝑘 é dado e que 𝑘 ≤ 𝑛 × 2

#### a. Formule o problema CSP

X = {k | k ≤ n × 2}

D = {x, y | 0 ≤ x n, 0 ≤ y ≤ n}

C = {{x + 1, y + 2} = vazio, {x - 1, y + 2} = vazio}, {x + 1, y - 2} = vazio, {x - 1, y - 2} = vazio}

#### b. Considere agora o problema de colocar no tabuleiro tantos cavalos quanto for possível, sem que nenhum seja atacado. Explique como resolver esse problema usando uma busca local a partir da definição adequada da funções AÇÃO e RESULTADO e da função objetivo

### **2.** Dê uma formulação CSP precisa para o seguinte problema: Alocação de Disciplinas: Existe um número fixo de professores e de salas de aula, uma lista de disciplinas a serem oferecidas e uma lista de possíveis horários para as disciplinas. Cada professor tem um conjunto de disciplinas que ele(a) pode lecionar

X = {professores}

D = {cada professor possui uma lista de disciplinas que lecionará}

C = {para cada lista disciplina de um professor, não pode haver disciplinas no mesmo horário, e elas devem ser distribuídas aos professores igualmente}

### **3.** Mostre como uma única restrição ternária do tipo 𝐴 + 𝐵 = 𝐶 pode se tornar três restrições binárias através do uso de uma variável auxiliar. Você pode assumir domínios finitos (Dica: Considere uma nova variável que recebe valores que são pares de outros valores, e considere restrições do tipo “X é o primeiro elemento do par Y”). Em seguida, mostre como restrições com mais do que três variáveis podem ser tratadas de forma similar. Finalmente, mostre como restrições unárias podem ser eliminadas pela alteração do domínio das variáveis. Isto completa a demonstração de que qualquer CSP pode ser transformado em um CSP com apenas restrições binárias

A + B = C

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
