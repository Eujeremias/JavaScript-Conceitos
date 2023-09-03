# UM BREVE DESAFIO SOBRE JAVASCRIPT 📝
Este desafio não trata-se de separar quem mais sabe ou sabe menos, pelo contrário, tem finalidade de disseminar conceitos tão simples que por serem como tal, passam despercebidos. Os conceitos abordados podem servir facilmente como critério eliminatório em entrevistas de empregos para uma vaga de Dev. **O importante é aprender!**

## Qual seria a definição correta de escopo?🤔

A definição de escopo trata-se da delimitação de uma variável no código. Uma variável declarada dentro de uma função, por exemplo, não pode ser acessada fora da mesma. A este tipo, nomeamos como **Escopo Local**. Já para as variáveis declaradas fora de uma função, chamamos este tipo de **Global Escopo**.

## Qual a diferença das seguintes declarações de variáveis: VAR, LET, CONST?🤔

Quando falamos sobre variável, é bom termos em mente as seguintes características: 1-Escopo | 2-Redeclaração | 3-Hoisting

Isso quer dizer que, esses três tipos de declarações de variáveis irão ter comportamentos diferentes em relação ao **escopo**, **redeclaração** e **hoisting**

### Escopo
O que delimita o acesso a uma função é justamente o escopo, se declararmos uma variável dentro de uma função e retornarmos ela, fora da função caso queiramos mostrar no console a variável, não conseguiremos.
### Redeclaração
A redeclaração consiste em atribuir outro valor a uma variável já declarada.

### Hoinsting
Trata-se da eleveção ao topo do escopo de uma variável. O JavaScript, antes mesmo de inicializar um código, ele eleva todos as declarações de uma variável ao todo do escopo. Ou seja, mesmo se imprima no console a variável antes de declará-la, você obterá um valor peculiar, experimente fazer isto.

1. VAR: A mesma tem escopo global, possibilidade de redeclaração (podemos até mesmo criar a mesma variável e alterar o seu valor) e sofre com hosting da seguinte forma: quando imprimimos no console a variável declarada após um console.log(), ela retornará undefined, isto por caus do hoisting

2. LET: Ela tem escopo local, portanto seu escopo irá até o fim da delimitação de um bloco. Sua redeclaração é de semelhante a do tipo VAR, entretanto você não pode criar novamente uma variável já existente, coisa que se pode fazer no VAR. Já o seu hoisting é diferente, se tentar dar um "log" numa variável que so será criada depois, dará um erro.

3. CONST: É semelhante ao let, porém o seu valor é constante, não pode ser alterado! Entretanto é interessante o seu comportamento quando se refere a objetos. Imagine uma const que recebe um objeto que por sua vez tem propriedades e valores. Podemos sim alterar o valor de uma propriedade pois, a princípio a const aponta para o próprio objeto, não para o valor da propriedade.

## Qual a diferença entre as seguintes expressões: function MyFunc(){...} e var MyFunn = function(){...} 

É simples, a primeira função poderá ser executada no início do script, já a segunda, só depois da sua inicialização