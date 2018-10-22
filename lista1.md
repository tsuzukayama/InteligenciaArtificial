# Lista 1

## Inteligência Artificial

### **1.** Defina com suas próprias palavras: (a) inteligência, (b) inteligência artificial, (c) agente, (d) racionalidade, (e) raciocínio lógico

* **Inteligência:** habilidade de aprender e aplicar novos conhecimentos e habilidades.
* **Inteligência artificial:** habilidade de softwares de computador de aprender e aplicar novos conhecimentos e habilidades.
* **Agente:** aquele que age e reage de acordo com o ambiente.
* **Racionalidade:** decisões tomadas.
* **Raciocínio lógico:** caminho percorrido para se tomar uma decisão.

### **2.** Ações reflexas (por exemplo, afastar a mão imediatamente ao tocar um objeto muito quente) são racionais? Elas são inteligentes?

Sim, pois não tomar a ação resulta em prejuízos (queimadura). Mas não são inteligentes, pois não é baseada em aplicar conhecimento adquirido.

### **3.** “Computadores não podem ser inteligentes – eles podem fazer apenas o que seus programadores dizem a eles”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

É verdadeira, computadores só fazem aquilo que são programados para fazer. Não, pois o programador pode ensinar habilidades para tomar decisões e aprender com elas.

### **4.** “Certamente animais não podem ser inteligentes – eles podem fazer apenas o que seus genes dizem a eles”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

--Todo--

### **5.** Certamente animais, computadores e humanos não podem ser inteligentes – eles podem fazer apenas o que os átomos que os constituem são obrigados a fazer pelas leis da física”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

--Todo--

## Agentes

### **1.** Para cada uma das seguintes atividades, forneça a descrição PEAS da tarefa a caracterize-a de acordo com as propriedades [Observável/Não observável; Determinístico/Estocástico; Episódico/Sequencial; Estático/Dinâmico; Discreto/Contínuo; Conhecido/Desconhecido]

#### Jogando futebol

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogadores, juíz|Velocidade, habilidade|Campo, bola, adversário|Chutar, passar bola|Visão, tato

Observável, estocástico, sequencial, dinâmico, contínuo, conhecido.

#### Explorando os oceanos subterrâneos de Titan

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Submarino|Seguro, Iluminar|Oceano, vida marinha|Navegar, iluminar|Visão, tato

Não observável, estocástico, sequêncial, dinâmico, contínuo, desconhecido.

#### Comprando livros de IA usados na internet

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Comprador|Seguro, confiável|Sites da internet|Navegar páginas, escolher livro mais barato|Leitor de tela

Observável, determinístico, episódico, estático, discreto, desconhecido.

#### Jogando uma partida de tênis

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogadores, Juíz|Acertar bola dentro da quadra|Quadra, Bola|, sacar, movimentar|Visão, tato

Observável, estocástico, sequencial, dinâmico, contínuo, conhecido.

#### Praticando tênis na (contra a) parede

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogador|Acertar bola dentro da quadra|Quadra, bola, parede|movimentar|Visão, tato

Observável, determinístico, sequencial, dinâmico, contínuo, conhecido.

#### Praticando salto em altura (atletismo)

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Atleta|Saltar o mais longe possível, a partir da marca de salto|Pista de salto|Correr, saltar, cair|Visão, tato

Observável, determinístico, sequencial, estático, contínuo, conhecido.

#### Tricotando um suéter

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Pessoa tricotando, |Habilidade|Cadeira, agulhas|tricotar|Visão, tato

Observável, determinístico, sequencial, estático, discreto.

#### Fazendo lances em um leilão

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Cliente|Cobrir lançes, saber quando parar|Local do leilão|Efetuar lançe|Visão, preço do lance

Observável, estocástico, episódico, dinâmico, contínuo.

### **2.** Defina os seguintes termos com suas próprias palavras: agente, função de agente, programa de agente, racionalidade, autonomia, agente reativo (reflexivo), agente baseado em modelo, agente baseado em objetivo, agente baseado em utilidade

#### Agente

Um agente é definido pelo ambiente que ele consegue perceber através de seus sensores e as ações que ele pode escolher para atingir um certo objetivo.

#### Função do agente

Entender o ambiente ao seu redor, e executar ações a partir deste entendimento, para chegar a um objetivo final.

#### Programa de agente

Tradução de um agente para linhas de código.

#### Racionalidade

Habilidade de maximizar seu desempenho, em cada tomada de decisão.

#### Autonomia

Habilidade de tomar decisões.

#### Agente reativo

Desenvolve sua inteligência a partir do ambiente, sem modelo estabelecido

#### Agente baseado em modelo

Possui um modelo interno que mapeia o mundo, e pode utilizar estados passados para tomar decisões futuras.

#### Agente baseado em objetivo

Toma suas decisões visando alcançar um objetivo final.

#### Agente baseado em utilidade

Toma suas decisões visando alcançar um objetivo final, levando em conta a probabilidade de sucesso.

### Implemente um agente reativo (reflexivo) simples para o problema do aspirador de pó automático, considerando o mundo de dois quadriculados (Figura 2.2 do livro) e as especificações da página 38. Simule o ambiente com este agente para todas as possíveis configurações iniciais sujo/limpo e posição do agente. Grave a medida de desempenho para cada configuração e o desempenho médio geral

```python
def reflex(perception)
  loc, status = perception
  if status == "sujo":
    limpa()
  if loc == "A":
    direita()
  else: esquerda()
```

Desempenho: nº de ações limpar() executadas, nº de vezes que A e B estão limpos.

### **4.** Considere uma versão modificada do problema do aspirador de pó automático, no qual a geografia do ambiente – extensão, limites e obstáculos – e as condições iniciais (quadriculados limpos/sujos) são desconhecidos. (Assuma que o agente pode se movimentar para cima, baixo, direita e esquerda.)

--Todo--