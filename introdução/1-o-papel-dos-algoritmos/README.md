# 1 -> Papel dos algoritmos na computação

###  `<-` [Voltar ao sumário](https://github.com/1luizneto/algoritmos-teoria-e-pratica/tree/main)

## 1.1 Algoritmos

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

## 1.2 Algoritmos como tecnologia

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
