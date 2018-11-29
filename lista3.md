# Lista 3

## MDP

### Capítulo 16

#### **2.** Chris avalia 4 carros usados antes de comprar aquele que tem a maior utilidade esperada. Pat avalia 10 carros e também deseja comprar o de maior utilidade esperada. Considerando condições de análise iguais para Chris e Pat, quem tem mais chances de comprar o melhor carro? Quem tem mais chances de se arrepender da qualidade do carro? Você conseguiria quantificar essas chances em termos do desvio padrão da qualidade esperada?

Suponha que existam **n** carros e dois estados diferentes, escolher o melhor carro ou não. A utilidade esperada para escolher o melhor carro dentre **n** carros é

![EU(S_{i}) = \sum_{i}^{n} p \cdot  U(s_{i})](https://latex.codecogs.com/gif.latex?EU(S_{i})&space;=&space;\sum_{i}^{n}&space;p&space;\cdot&space;U(s_{i}))

![EU(S_{i}) = \sum_{i}^{n} p \cdot  1](https://latex.codecogs.com/gif.latex?EU(S_{i})&space;=&space;\sum_{i}^{n}&space;p&space;\cdot&space;1)

![EU(S_{i}) = n \cdot p](https://latex.codecogs.com/gif.latex?EU(S_{i})&space;=&space;n&space;\cdot&space;p)

Chris tem ``U(s) = 4p`` e Pat tem ``U(s) = 10p``.


#### **3.** Em 1713, Nicolas Bernoulli formulou um puzzle, agora conhecido como "o paradoxo de São Petersburgo", que funciona da seguinte maneira.  Você tem a oportunidade de jogar um jogo no qual uma moeda justa é lançada repetidamente até que o resultado seja "cara". A primeira vez que aparecer "cara" no n-ésimo lançamento, você ganha 2^n reais

##### a) Mostre que o valor monetário esperado desse jogo é infinito
```
EMV(L) = somatória de n até infinito, da probabilidade de cara aparecer na jogada n vezes a utilidade esperada.

EMV(L) = SOMA(1 até infinito, 2^-n * 2^n)
EMV(L) = SOMA(1 até infinito, 1)
EMV(L) = infinito
```

##### b) Quanto você pagaria para jogar esse jogo?
```
n = 1, U = 2, P = 0.5
n = 2, U = 4, P = 0.25
n = 3, U = 8, P = 0.125
```

Em torno de 4 reais, pois para ganhar mais que isso, a probabilidade já é muito baixa.

##### c) Daniel Bernoulli, primo de Nicolas, resolveu o aparente paradoxo em 1738 sugerindo que a utilidade monetária fosse medida usando uma escala logarítmica (ou seja, *U(S<sub>n</sub>) = a * log2 n + b*, em que *S<sub>n</sub>* é o estado com *R$n*). Qual é a utilidade esperada para o jogo sob essa suposição.

Assumindo o patrimonio inicil de (k - c), onde c é o preço do jogo:

```
U(L) = somatoria(1 até infinito, 2^-n * a * log2(k - c + 2^n) + b);
```

Assumindo k - c = 0 para simplificar:
```
U(L) =  somatoria(1 até infinito, 2^-n * (a * log2(2^n) + b);
U(L) =  somatoria(1 até infinito, 2^-n * a * n + b;
U(L) = 2 * a + b;
```

##### a) Qual seria a quantidade máxima que alguém pagaria para jogar o jogo, assumindo que essa pessoa já possui *R$k*?

```
a * log2c + b = 2 * a + b;
c = 4;
```

### Capítulo 17

#### **1.** Para o mundo 4 × 3 mostrado na Figura 17.1, calcule quais quadrados podem ser alcançados a partir de (1, 1),  pela sequência de ações [cima, cima, direita, direita, direita] e com quais probabilidades.



#### **3.** Suponha que nós definimos a utilidade de uma sequência de estados para ser a máxima recompensa obtida em qualquer estado da sequência. Mostre que esta função utilidade não resulta em preferências estacionárias entre sequências de estado. Seria possível definir uma função utilidade em estados tal que a decisão por máxima utilidade esperada (MEU) resulta no comportamento ótimo do agente?



#### **5.** Para o ambiente mostrado na Figura 17.1, encontre os valores limites *(threshold)* para *R(s)* tal que a política ótima muda quando o valor limite é cruzado. Você irá precisar calcular a política ótima e seu valor fixo *R(s)*. Dica: Prove que o valor de qualquer política fixa varia linearmente com *R(s)*.

#### **8.** Considere o mundo 3 × 3 mostrado na Figura 17.14(a). O modelo de transição é mesmo que aquele do mundo 4 × 3 na Figura 17.1: 80% do tempo o agente vai na direção que ele seleciona; no restante do tempo ele vai em direção ortogonal àquela pretendida. Implemente o algoritmo de valor-iteração para este mundo para cada um dos valores de *r* abaixo. Use recompensas com desconto com um fator de g = 0.99. Mostre a política obtida em cada caso. Explique intuitivamente por que o valor de *r* leva a cada política.

##### a) *r* = 100

##### b) *r* = -3

##### c) *r* = 0

##### d) *r* = +3

#### **10.** Considere um MDP com três estados, (1, 2, 3), com recompensas −1, −2, 0, respectivamente. O estado 3 é um estado terminal. Nos estados 1 e 2, há duas ações possíveis: *a* e *b*. O modelo de transição é como segue:<br /><br />• No estado 1, a ação *a* move o agente para o estado 2 com probabilidade 0.8 ou faz com que o agente permaneça no mesmo estado com probabilidade 0.2.<br />• No estado 2, a ação *a* move o agente para o estado 1 com probabilidade 0.8 ou faz com que o agente permaneça no mesmo estado com probabilidade 0.2.<br />• No estado 1 ou estado 2, a ação *b* move o agente para o estado 3 com probabilidade 0.1 ou faz com que o agente permaneça no mesmo estado com probabilidade 0.9.<br /><br />Com base nisso, responda as seguintes questões:

##### a) O que pode ser determinado qualitativamente sobre a política ótima nos estados 1 e 2?

##### b) Aplique o algortimo de política-iteração, mostrando cada passo, para determinar a política ótima e os valores dos estados 1 e 2. Assuma que a política inicial tem ação *b* em ambos os estados

##### c) O que acontece com o algoritmo de política-iteração se a política inicial tem ação *a* em ambos os estados? Aplicar desconto ajuda? A política ótima depende do fator de desconto?