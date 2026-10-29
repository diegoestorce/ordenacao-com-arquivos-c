Ordenação com Arquivos em C

Programa em C que une algoritmos de ordenação com manipulação de arquivos. Ele grava valores numéricos desordenados em um arquivo, lê esses valores, ordena com o algoritmo escolhido pelo usuário e salva o resultado em um novo arquivo. Também permite alterar um valor do arquivo original e reordenar.

Projeto desenvolvido como Atividade Avaliativa 03 na UNICID.

Funcionalidades
Criar o arquivo dados.txt com valores desordenados, digitados pelo usuário ou gerados aleatoriamente (de 1 a 100 valores).
Ler e exibir o conteúdo de dados.txt.
Escolher o algoritmo de ordenação, ordenar e salvar o resultado em ordenado.txt.
Alterar um valor de dados.txt pela posição e reordenar, atualizando os dois arquivos.
Exibir o conteúdo de ordenado.txt.
Algoritmos implementados
Algoritmo	Estratégia	Complexidade média
Bubble Sort	Comparação e troca	O(n²)
Insertion Sort	Inserção ordenada	O(n²)
Selection Sort	Seleção do menor	O(n²)
Merge Sort	Dividir e conquistar	O(n log n)
Quick Sort	Dividir e conquistar	O(n log n)
Arquivos utilizados
Arquivo	Conteúdo
dados.txt	Valores originais (entrada), um por linha
ordenado.txt	Valores já ordenados (saída), um por linha

Os dois arquivos são criados na pasta de onde o programa é executado.

Como compilar e executar

É necessário ter um compilador C, como o GCC.

bash
gcc atividade03.c -o atividade03
./atividade03

No Windows, execute atividade03.exe (ou atividade03 no terminal).

Menu do programa
===== ORDENACAO COM ARQUIVOS =====
1 - Criar dados.txt (valores desordenados)
2 - Ler e exibir dados.txt
3 - Ordenar e salvar em ordenado.txt
4 - Alterar um valor e reordenar
5 - Exibir ordenado.txt
0 - Sair
Exemplo de uso
Escolha a opção 1 para criar o dados.txt com 5 valores: 9 3 7 1 8.
Escolha a opção 3 e depois o algoritmo 5 (Quick Sort):
Antes:  9 3 7 1 8
Depois: 1 3 7 8 9

Ordenado com Quick Sort e salvo em ordenado.txt.
Escolha a opção 4, altere a posição 2 para o valor -4 e escolha o Merge Sort:
Alterando posicao 2: 3 -> -4
Arquivo dados.txt atualizado.

Antes:  9 -4 7 1 8
Depois: -4 1 7 8 9

Ordenado com Merge Sort e salvo em ordenado.txt.
Conceitos utilizados
Arquivos: fopen (modos "w" e "r"), fprintf, fscanf e fclose, com verificação de erro na abertura.
Ponteiros: troca de valores com ponteiros, vetores passados como ponteiros e alocação dinâmica (malloc e free) no Merge Sort.
Estrutura switch: menu principal e escolha do algoritmo.
Funções: o código é dividido em funções para arquivos, ordenação e opções do menu.
Limitações
Trabalha apenas com números inteiros.
Aceita no máximo 100 valores. Se o dados.txt tiver mais que isso, ou texto inválido, o programa recusa o arquivo para não perder dados.
A alteração de valor é feita pela posição (começando em 1).
