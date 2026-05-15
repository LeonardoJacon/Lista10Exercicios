# Lista de Exercícios - Estrutura de Dados em C
---
## Segundo Bimestre

## Exercício 1 — Fibonacci Recursivo (Sem Memoização)
## Descrição

O programa calcula um termo da sequência de Fibonacci utilizando recursão simples, sem otimizações.

Além do resultado, o programa exibe a quantidade total de chamadas recursivas realizadas para demonstrar a ineficiência da abordagem ingênua.

## Funcionamento

A sequência de Fibonacci é definida por:

F(n)=F(n−1)+F(n−2)

Com os casos base:

F(0)=0

F(1)=1

##Lógica da Solução

A função recursiva divide o problema em dois subproblemas menores:

fib(n-1)
fib(n-2)

A recursão continua até atingir os casos base.

A solução recalcula vários valores repetidamente, aumentando muito a quantidade de chamadas recursivas.

Caso Base
if (n == 0)
    return 0;

if (n == 1)
    return 1;
Redução do Problema
return fibonacci(n - 1, chamadas) +
       fibonacci(n - 2, chamadas);
       ---
## Exercício 2 — Fibonacci com Memoização

## Descrição

O programa resolve o mesmo problema do exercício anterior, porém utilizando memoização com alocação dinâmica.

Os resultados já calculados são armazenados em memória para evitar recálculos desnecessários.

O programa também compara a quantidade de chamadas da versão ingênua e da versão otimizada.

O que é Memoização

Memoização é uma técnica de otimização onde resultados já calculados são armazenados para reutilização futura.

## Funcionamento

Um vetor alocado dinamicamente é utilizado como cache:

long long *cache = malloc((n + 1) * sizeof(long long));

Os valores inicialmente recebem -1, indicando que ainda não foram calculados.

Antes de calcular um valor, o programa verifica:

if (cache[n] != -1)
    return cache[n];

Se o valor já existir no cache, ele é retornado imediatamente.

Vantagens da Memoização
Evita cálculos repetidos
Reduz drasticamente as chamadas recursivas
Melhora significativamente o desempenho
Caso Base
if (n == 0)
    return 0;

if (n == 1)
    return 1;
Redução do Problema
cache[n] =
    fibonacciMemo(n - 1, cache, chamadas) +
    fibonacciMemo(n - 2, cache, chamadas);
    ---
## Exercício 3 — Torres de Hanoi
## Descrição

O programa resolve o problema das Torres de Hanoi utilizando recursão.

O usuário informa a quantidade de discos, e o programa exibe todos os movimentos necessários para mover os discos da torre de origem até a torre de destino.

Regras do Problema
Apenas um disco pode ser movido por vez
Um disco maior nunca pode ficar sobre um disco menor
Funcionamento

A solução recursiva segue três passos:

Mover n-1 discos para a torre auxiliar
Mover o maior disco para a torre destino
Mover novamente n-1 discos para a torre destino
Caso Base

Quando existe apenas um disco:

if (n == 1)

O disco é movido diretamente.

Redução do Problema
hanoi(n - 1, origem, auxiliar,
      destino, movimentos);

e depois:

hanoi(n - 1, auxiliar, destino,
      origem, movimentos);
Quantidade de Movimentos

A quantidade mínima de movimentos é dada por:

M(n)=2
n
−1

Tecnologias Utilizadas
Linguagem C
Recursão
Memoização
Alocação dinâmica de memória
Restrições Atendidas
Uso obrigatório de recursão
Sem variáveis globais
Memoização com memória dinâmica
Caso base explícito
Sem bibliotecas prontas para resolver os exercícios
Compilação e Execução
Compilar
gcc arquivo.c -o programa
Executar
./programa
Conclusão

Os exercícios demonstram o funcionamento da recursão e mostram a diferença entre uma solução recursiva ingênua e uma solução otimizada com memoização.

Também foi possível observar como a recursão divide problemas grandes em subproblemas menores até atingir o caso base.
---
---
##  Descrição

Este repositório contém a resolução de 10 exercícios em linguagem C, abordando conceitos fundamentais como vetores, matrizes, ponteiros, structs e alocação dinâmica de memória.

## Primeiro Bimestre
##  Explicação das Soluções

### 1. Inversão de palavras

Foi utilizado um vetor bidimensional de caracteres para armazenar 3 palavras.
Após a leitura, um laço for percorre o vetor de trás para frente, exibindo as palavras em ordem inversa.

---

### 2. Vetor inverso

Foi criado um vetor de 5 posições para armazenar números inteiros.
Os valores são lidos e depois exibidos em ordem inversa utilizando um laço decrescente.

---

### 3. Matriz multiplicada

Uma matriz 3x3 é preenchida com valores informados pelo usuário.
Em seguida, cada elemento da matriz é multiplicado por 5 utilizando dois loops aninhados.

---

### 4. Matriz identidade

Foi criada uma matriz identidade (1 na diagonal principal e 0 no restante).
Depois, foi realizada a multiplicação da matriz original pela identidade, comprovando que o resultado é a própria matriz original.

---

### 5. Multiplicação vetor x matriz

Um vetor de 3 posições e uma matriz 3x3 são lidos.
A multiplicação é feita percorrendo as colunas da matriz e acumulando os resultados em um vetor resultado.

---

### 6. Cadastro de alunos

Foi utilizada uma struct para armazenar nome, matrícula e média.
Os alunos são classificados em aprovados e reprovados com base na média (>= 5.0), sendo armazenados em vetores separados.

---

### 7. Sistema de busca de livros

Foi criada uma struct para armazenar dados de livros.
Após o cadastro, o usuário informa um título e o programa busca utilizando strcmp para comparar strings.

---

### 8. Vetor com ponteiros

Um vetor de inteiros foi manipulado utilizando apenas aritmética de ponteiros.
Os valores são acessados com (p + i) e exibidos com o dobro.

---

### 9. Ordenação com ponteiros

Uma função recebe três valores por referência (ponteiros).
Os valores são ordenados diretamente nas variáveis originais usando trocas (swap).
A função também verifica se os três valores são iguais.

---

### 10. Maior nota com alocação dinâmica

Foi utilizado malloc para alocar dinamicamente um vetor de alunos.
Uma função percorre o vetor usando ponteiros e retorna o aluno com maior nota.

---

##  DESAFIO 1 — Expressão Balanceada (Pilha)

Foi utilizada uma pilha dinâmica para verificar se uma expressão está balanceada.

Durante a leitura da expressão, cada símbolo de abertura é inserido na pilha. Ao encontrar um símbolo de fechamento, o programa remove o topo da pilha e verifica se os símbolos correspondem corretamente.

Se houver incompatibilidade ou tentativa de remoção em pilha vazia, a expressão é considerada inválida.

Ao final, se a pilha estiver vazia, a expressão é válida.

---

##  DESAFIO 2 — Inversão de String com Pilha

A pilha foi utilizada para inverter uma string respeitando a lógica LIFO.

Cada caractere da string é inserido na pilha. Em seguida, os caracteres são removidos um a um, resultando na inversão da ordem original.

A inversão ocorre naturalmente devido ao comportamento da pilha, onde o último elemento inserido é o primeiro a ser removido.

---
##  DESAFIO 3 — Fila de Clientes (FIFO)

Foi implementada uma fila encadeada utilizando ponteiros para representar o início e o fim da fila.

Os clientes são inseridos no final da fila por meio da operação enqueue. Durante o atendimento, os clientes são removidos do início da fila utilizando dequeue, respeitando a ordem de chegada (FIFO).

O tempo de espera de cada cliente é calculado acumulando os tempos de atendimento dos clientes anteriores, garantindo que cada cliente aguarde corretamente sua vez.

---

##  DESAFIO 4 — Fila de Impressão com Prioridade

Foi implementada uma fila encadeada com inserção ordenada por prioridade.

Ao inserir um novo documento, o programa percorre a fila até encontrar a posição correta, garantindo que documentos com menor valor de prioridade sejam atendidos primeiro.

Em casos de empate, o novo elemento é inserido após os já existentes, mantendo a ordem de chegada.

A remoção dos documentos é feita sempre a partir do início da fila.

---

## Tecnologias

* Linguagem C
* Compilador GCC

---

## Como executar

1. Compile o código:

gcc nome_do_arquivo.c -o programa


2. Execute:

./programa

