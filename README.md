# Lista de Exercícios - Estrutura de Dados em C

##  Descrição

Este repositório contém a resolução de 10 exercícios em linguagem C, abordando conceitos fundamentais como vetores, matrizes, ponteiros, structs e alocação dinâmica de memória.

---

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

