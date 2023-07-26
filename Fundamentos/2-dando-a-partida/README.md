# 2 Dando a partida

###  `<-` [Voltar ao sumário](https://github.com/1luizneto/algoritmos-teoria-e-pratica/tree/main)

##

### Insertion Sort

```c++
/**
* @brief Ordena um array de inteiros usando o algoritmo de InsertionSort.
*
* @param array O array a ser ordenado.
*/
void insertionSort(vector<int> &array) {
  // Percorre o array a partir do segundo elemento.
  for (int j = 1; j < array.size(); j++) {
    // Obtém o valor do elemento atual do array.
    int chave = array[j];

    // Inicializa o índice do elemento anterior ao elemento atual.
    int i = j - 1;

    // Percorre o array a partir do elemento anterior ao elemento atual,
    // comparando o valor do elemento atual com os elementos anteriores.
    // Se o valor do elemento atual for menor do que um dos elementos anteriores,
    // os elementos são trocados de posição.
    while (i >= 0 && array[i] > chave) {
      array[i + 1] = array[i];
      i = i - 1;
    }

    // Coloca o elemento atual na posição correta.
    array[i + 1] = chave;
  }
}
```

##

## Exercícios 2.1

2.1-1 Usando a Figura 2.2 como modelo, ilustre a operação de Insertion-Sort no arranjo A = 〈31, 41, 59, 26, 41, 58〉.

##

2.1-2 Reescreva o procedimento Insertion-Sort para ordenar em ordem não crescente, em vez da ordem não decrescente.

##

2.1-3 Considere o problema de busca:

Entrada: Uma sequência de n números A = 〈a1, a2, ..., an〉 e um valor v.

Saída: Um índice i tal que v = A[i] ou o valor especial NIL, se v não aparecer em A.

Escreva o pseudocódigo para busca linear, que faça a varredura da sequência, procurando por v. Usando um invariante de laço, prove que seu algoritmo é correto. Certifique-se de que seu invariante de laço satisfaz as três propriedades necessárias.

##

2.1-4 Considere o problema de somar dois inteiros binários de n bits, armazenados em dois arranjos de n elementos A e B. A soma dos dois inteiros deve ser armazenada em forma binária em um arranjo de (n + 1) elementos C. Enuncie o problema formalmente e escreva o pseudocódigo para somar os dois inteiros.

##

### 2.2 Análise de algoritmos

Analisar um algoritmo é prever quanto de recursos um algoritmo necessita para ser executado.

O tempo de execução de um algoritmo pode variar de acordo com o ambiente e diversas formas de execução, normalmente são analisados em geral o tamanho da entrada e o tempo de execução. A análise de eficiência de um algoritmo pode ser feita de várias formas mas normalmente é buscado utilizar formas mais simples e de fácil compreensão para se ter um resultado.

No geral são analisados os tempos de execução de um algoritmo nos piores casos. Normalmente utilizado como base a ordem de crescimento e definindo a eficiência do algoritmo com base neste dado simplificado, assim um algoritmo é mais eficiente que outro caso apresente uma ordem de crescimento (Θ) mais baixa.

##

## Exercícios 2.2

2.2-1 Expresse a função n3/1000 − 100n2− 100n + 3 em termos da notação Θ.

##

2.2-2 Considere a ordenação de n números armazenados no arranjo A, localizando primeiro o menor elemento de A e permutando esse elemento com o elemento contido em A[1]. Em seguida, determine o segundo menor elemento de A e permute-o com A[2]. Continue dessa maneira para os primeiros n − 1 elementos de A. Escreva o pseudocódigo para esse algoritmo, conhecido como ordenação por seleção. Qual invariante de laço esse algoritmo mantém? Por que ele só precisa ser executado para os primeiros n − 1 elementos, e não para todos os n elementos? Forneça os tempos de execução do melhor caso e do pior caso da ordenação por seleção em notação Θ.

##

2.2-3 Considere mais uma vez a busca linear (veja Exercício 2.1-3). Quantos elementos da sequência de entrada precisam ser verificados em média, considerando que o elemento que está sendo procurado tenha a mesma probabilidade de ser qualquer elemento no arranjo? E no pior caso? Quais são os tempos de execução do caso médio e do pior caso da busca linear em notação Θ? Justifique suas respostas.

Θ(n/2)?

Pior caso busca linear: Θ(n), pode ser necessário ter que passar por todos os elementos para encontrar o alvo no ultimo item, ou nem encontrá-lo.

##

2.2-4 Como podemos modificar praticamente qualquer algoritmo para ter um bom tempo de execução no melhor caso?

##

### 2.3 Projeto de algoritmos

Divisão e conquista: Muitos algoritmos são recursivos, para resolver um problemas eles chamam eles mesmos recursivamente uma ou mais vezes para lidar com subproblemas. Normalmente esses algoritmos seguem uma abordagem de divisão e conquista desmembrando o problema em vários subproblemas menores semelhantes ao original.

##

## Exercícios 2.3
2.3-1 Usando a Figura 2.4 como modelo, ilustre a operação de ordenação por intercalação para o arranjo A = 〈3, 41, 52, 26, 38, 57, 9, 49〉.

2.3-2 Reescreva o procedimento Merge de modo que ele não utilize sentinelas e, em vez disso, pare tão logo todos os elementos do arranjo L ou do arranjo R tenham sido copiados de volta em A e então copie o restante do outro arranjo de volta em A.

2.3-3 Use indução para mostrar que, quando n é uma potência exata de 2, a solução da recorrência é T(n) = n lg n.

2.3-4 A ordenação por inserção pode ser expressa como um procedimento recursivo da maneira descrita a seguir. Para ordenar A[1 .. n], ordenamos recursivamente A[1 .. n − 1] e depois inserimos A[n] no arranjo ordenado A[1 .. n − 1]. Escreva uma recorrência para o tempo de execução de pior caso dessa versão recursiva da ordenação por inserção.

2.3-5 Voltando ao problema da busca (ver Exercício 2.1-3) observe que, se a sequência A for ordenada, poderemos comparar o ponto médio da sequência com v e não mais considerar metade da sequência. O algoritmo de busca binária repete esse procedimento, dividindo ao meio o tamanho da porção restante da sequência a cada vez. Escreva pseudocódigo, iterativo ou recursivo, para busca binária. Demonstre que o tempo de execução do pior caso da busca binária é Θ(lg n).

2.3-6 Observe que o laço while das linhas 5 a 7 do procedimento Insertion-Sort na Seção 2.1 utiliza uma pesquisa linear para varrer (no sentido inverso) o subarranjo ordenado A[1 .. j − 1]. Podemos usar, em vez disso, uma busca binária (veja Exercício 2.3-5) para melhorar o tempo de execução global do pior caso da ordenação por inserção para Θ(n lg n)?

2.3-7 Descreva um algoritmo de tempo Θ(n lg n) que, dado um conjunto S de n inteiros e um outro inteiro x, determine se existem ou não dois elementos em S cuja soma seja exatamente x.
