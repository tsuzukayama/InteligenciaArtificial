# Lista 4

## Heurísticas, meta-heurísticas

### 1. Por que o uso de meta-heurísticas pode ser interessante para resolver problemas?

Quando um problema é muito difícil de se mapear, visualizar, etc., o uso de heurísticas pode ser bom, pois ela permite encontrar soluções que não são necessáriamente racionais. 

É boa para problemas onde os ambientes:

* São parcialmente ou não observáveis;
* São aleatórios;
* Possuem muitos estados;
* Não possuem um objetivo definido.

### 2. Quais as vantagens de utilizar o algoritmo Simulated Annealing ao invés do Hillclimbing? Existe algum caso em que seria mais vantajoso utilizar Hill-climbing ao invés do simulated annealing?

Hill climbing: vai avaliar os vizinhos, e, se forem de valor maior, caminha em sua direção. Sempre encontra o máximo local.

Simulated annealing: o próximo estado a ser observado é aleatório. Se este for melhor que o anterior, é feita a substituição. Caso contrário, ele pode ser substituido a partir de uma probabilidade dada por uma função objetivo e uma temperatura, que é reduzida a cada iteração.

Vantagens do hill climbing: por ser aleatório, o simulated annealing não é muito performático. Em contra partida, quando o hill climbing encontrar um estado "bom", não irá mais substituir este, tendo performance razoável. Uma boa alternativa é a combinação dos dois algoritmos, onde é efetuado o hill climbing, mas também se procura novos estados melhores, efetuando a troca em certas condições.

### 3. (Baseado no Ex. 4.4 do Russel) Gere um número considerável de exemplos (condições iniciais) do problema 8-puzzle e resolva-os (se possível) usando o algoritmo Hill-climbing (subida mais íngreme e primeira escolha nas variantes) e simulated annealing. Meça o custo da busca e o percentual de problemas resolvidos. Comente os resultados.

### 4. (Baseado no Ex. 4.4 do Russel) Gere um número considerável de exemplos (condições iniciais) do problema 8-rainhas e resolva-os (se possível) usando o algoritmo Hill-climbing (subida mais íngreme e primeira escolha nas variantes), Hill-climbing com inicialização aleatória e simulated annealing. Meça o custo da busca e o percentual de problemas resolvidos. Comente os resultados.

### 5. No contexto de meta-heurísticas, defina com suas próprias palavras: busca local, função objetivo (fitness), busca local completa, busca local ótima, exploração, explotação, indivíduo, população.

* **Busca local:** parte de uma solução inicial qualquer e, iterativamente, caminha para soluções vizinhas até um ponto de convergência;
* **Função objetivo (fitness):** função que sumariza quão proximo uma solução está de atingir seu objetivo;
* **Busca local completa:** é completa se encontra um estado final;
* **Busca local ótima:** é ótima se encontra o melhor dos estados finais;
* **Exploração:** percorrer caminhos poucos ou não percorridos; 
* **Explotação:** recorçar o melhor caminho encontrado até então;
* **Indivíduo:** solução de um algoritmo genético; 
* **População:** conjunto de soluções de um algoritmo genético;

### 6. No contexto dos algoritmos genéticos (GA), defina a representação, cruzamento e mutação para o jogo Sudoku. Qual função objetivo (fitness) utilizar?

### 7. Realize os seguintes cruzamentos (crossovers) de um ponto

#### a. 000111 e 101010 com ponto de corte=4

#### b. 11011110 e 00001010 com ponto de corte=1

#### c. 1010 e 0101 com ponto de corte=2