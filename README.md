# Algoritmos Teoria e Prática
Eu resolvi criar esse repositório para colocar um resumo feito por mim e suas questões resolvidas em C++.

##
Cada capitulo do livro aborda um algoritmo com explicações e detalhes de forma simples para que possa ser replicado em qualquer linguagem, mas eu optei por usar C++.

## Sumário

### Introdução:
* `1` [O papel dos algoritmos na computação](Introcução/O-papel-dos-algoritmos/README.md)
 <a href="#1">1 Papel dos algoritmos na computação</a> <br>
 <a href="#1.1">_1.1 Algoritmos_</a> <br>
 <a href="1.2">_1.2 Algoritmos como tecnologia_</a> <br> 
 <a href="#2">2 Dando a partida</a> <br>
 <a href="#2.1">_2.1 Ordenação por inserção_</a>   
 <a href="#2.2">_2.2 Análise de algoritmos_</a> <br>
 <a href="#2.3">_2.3 Projeto de algoritmos_</a> <br>
 <a href="#3">3 Crescimento de funções</a> <br>

##
<br>
<br>
<br>


## 1 -> Papel dos algoritmos na computação

### 1.1 Algoritmos

Algoritmo de forma resumida e informal é qualquer procedimento computacional que recebe dados de entrada e retorna dados de saida, executando ações no meio do caminho.

I -> O

Algoritmos normalmente são ditados pelas regras e expectativas enunciadas para solução do problema, outro fator que também influência são os limites como memória/tempo/espaço. São iniciados com uma instância (valor de entrada) e seguem as regras programadas para retornar (sair) o esperado.

Algoritmos de ordenação normalmente são os primeiros a serem vistos e são necessários em muitos algoritmos posteriores como por exemplo a busca binária, ela precisa de dados ordenados antes de funcionar.

Um algoritmo é correto se para toda entrada ele retornar com a saída correta. Assim pode-se dizer que o algoritmo resolve o problema dado à ele.

As vezes um algoritmo "errado" pode ser útil se a taxa de erros for controlada. Mas na maioria dos casos concentre-se em algoritmos corretos.

##

### Estruturas de dados

São formas de armazenar e organizar os dados para que sejam mais fáceis de trabalhar em determinados momentos, não existe estrutura perfeita, cada uma funciona bem em determinadas condições.

##

### Problemas difíceis

Dentro da área de algoritmos existem alguns algoritmos chamados de NP-Completos que ainda não possuem uma solução eficiente, são algoritmos que seguindo determinadas regras não conseguirão entregar o resultado com eficiência. É bom conhecer esses algoritmos pois com certeza eles irão aparecer em algum momento da vida e sabendo que são "impossíveis" você pode abordá-los de maneira diferente.

Os NP-Completos não são impossiveis ou eternamente ineficientes, mas enquanto ninguém encontra uma solução eles são uma "magia negra" dos algoritmos.

[Explicação NP completo em artigo](https://segredo.dev/problemas-np/)

## Exercícios 1.1

1.1-1 Cite um exemplo real que exija ordenação ou um exemplo real que exija o cálculo de uma envoltória convexa.

R: Cálculo e ordenação de lista de vencedores das olimpiadas com base em número de medalhas. Lista telefônica em ordem alfabética, o alfabeto pode ser um tipo de ordenação.

##

1.1-1 Além da velocidade, que outras medidas de eficiência poderiam ser usadas em uma configuração real?

R: Memória, espaço, tipo de dispositivo de armazenamento.

##
1.1-3 Selecione uma estrutura de dados que você já tenha visto antes e discuta seus pontos fortes e suas limitações.

R: Array: Um ponto forte é a facilidade em acessar um dado sem ter que percorrer toda a estrutura (diferente de listas), ponto fraco é que para remover(do inicio)/reordenar elementos é usado muito processamento pois normalmente precisa reposicionar toda a estrutura para que os indices fiquem de acordo e a memória alocada esteja correta.

##
1.1-4 Em que aspectos os problemas anteriores do caminho mais curto e do caixeiro-viajante são semelhantes? Em que aspectos eles são diferentes?

R:
Semelhança: Ambos precisam calcular distâncias entre pontos e crescem de forma preocupante no número de cálculos conforme as rotas aumentam. Também ambos buscam encontrar a menor distância possível entre pontos.

Diferença: O caminho mais curto calcula apenas o ponto seguinte mais próximo ao invés de tentar traçar toda a rota completa.

##
1.1-5 Mostre um problema real no qual apenas a melhor solução servirá. Em seguida, apresente um problema em que baste uma solução que seja “aproximadamente” a melhor.

R:
Melhor solução: Determinar valores e transações financeiras de uma instituição. Os valores precisam ser exatos para haver um controle.

Aproximadamente: Determinar grau de similaridade com peso entre produtos ou categorias, uma taxa de erro é aceitável e a precisão não precisa ser exata, relacionando um número suficiente atende a funcionalidade.

##

### 1.2 Algoritmos como tecnologia

Por mais que os computadores fossem infinitamente poderosos os algoritmos ainda seriam úteis pela possibilidade de traçar e entregar resultados com previsibilidade. Assim poderia demonstrar que tal solução entrega a resposta correta.

No mundo real recursos computacionais são limitados e normalmente caros, algoritmos eficientes visam equilibrar esses recursos para entregar uma resposta adequada com a minima utilização dos recursos possivel.

##

### Eficiência

A eficiência de um algoritmo pode ser medida por vários fatores, mas normalmente só é notável com grandes números de dados de entrada, onde nestes você consegue ver uma grande diferença entre a escolha de um algoritmo certo e um menos eficiente. Isto pode impactar diretamente na funcionalidade de seu programa, a escolha de um algoritmo eficiente assim como hardware são fatores que devem ser considerados durante o desenvolvimento de um software.

Uma sólida base de conhecimento e técnica de algoritmos é uma das características que separam os programadores verdadeiramente qualificados dos novatos. Você pode executar algumas tarefas sem saber muito de algoritmos, mas com uma boa base de algoritmos é possível fazer muito mais!

Algoritmos estão presente em quase todas as tecnologias, sejam elas hardware ou software, provavelmente em algum pedaço haverá um algoritmo trabalhando para solucionar um problema.

##

## Exercícios 1.2
1.2-1 Cite um exemplo de aplicação que exige conteúdo algorítmico no nível da aplicação e discuta a função dos algoritmos envolvidos.

R: GPS em tempo real. Resumidamente o algoritmo de menor distância precisa ficar calculando a todo instante ao mesmo tempo que interage com outros algoritmos como direção das ruas e fluxo do trânsito.

##

1.2-2 Suponha que estamos comparando implementações de ordenação por inserção e ordenação por intercalação na mesma máquina. Para entradas de tamanho n, a ordenação por inserção é executada em 8n2 passos, enquanto a ordenação por intercalação é executada em 64n lg n passos. Para quais valores de n a ordenação por inserção supera a ordenação por intercalação?

##

1.2-3 Qual é o menor valor de n tal que um algoritmo cujo tempo de execução é 100n2 funciona mais rapidamente que um algoritmo cujo tempo de execução é 2n na mesma máquina?

##

## 2 Dando a partida

Insertion Sort

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

##

## 3 Crescimento de funções

A ordem de crescimento de tempo de execução de um algoritmo nos permite caracterizar a eficiência de um algoritmo e também nos permite comparar o desempenho de um algoritmo em relação a outro. Quando analisamos tamanhos de entrada estamos estudando a eficiência _assintótica_ do algoritmo. Ou seja, estamos preocupados em como o tempo do algoritmo aumenta de acordo com o tamanho de entrada no limite.

Em geral um algoritmo que é assintoticamente mais eficiente será a melhor escolha para todas as entradas, exceto as muito pequenas.
