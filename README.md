
# Lista de Exercícios JavaScript

Isac Ponciano Bandeira

## 1. O que é o ES6?

ES6 nada mais é que a especificação usada para implementar JavaScript.No
caso a nova versão do JS.

## 2. Exemplifique algumas features introduzidas no ES6

● Default parameters
Nos permite inicializar parâmetros com valores padrão, caso nenhum valor
tenha sido especificado, ou caso o valor seja undefined.

● RegExp flags "y" e "u"
A RegExp /y, também chamada de sticky, busca apenas a partir do índice
indicado pela propriedade lastIndex da expressão regular na string.

● Destructuring
É uma expressão JavaScript que torna possível extrair dados de qualquer
objeto que seja iterável e colocá-los em outras variáveis.

● Arrow Function
Uma expressão arrow function possui uma sintaxe mais curta quando
comparada a uma expressão de função (function expression) e não tem seu
próprio this, arguments, super ou new.target. Estas expressões de funções
são melhor aplicadas para funções que não sejam métodos, e elas não
podem ser usadas como construtoras (constructors).

● Escopo
É o contexto atual de execução, em que valores e expressões são "visíveis"
ou podem ser referenciadas. Se uma variável ou outra expressão não estiver
"no escopo atual", então não está disponível para uso. Os escopos também
podem ser em camadas em uma hierarquia, de modo que os escopos filhos
tenham acesso aos escopos país, mas não vice-versa.

● Desestruturação
A sintaxe de atribuição via desestruturação (destructuring assignment) é uma
expressão JavaScript que possibilita extrair dados de arrays ou objetos em
variáveis distintas.

## 3. Qual a diferença entre var, let e const?

var: No caso da palavra-chave var, além da variável ser içada (hoisting) ela é
automaticamente inicializada com o valor undefined (caso não seja atribuído
nenhum outro valor)
Exemplo:

var company = 'Hcode Treinamentos';
console.log('Minha empresa se chama ' + company);

Let: Onde a variável declarada com let leva em conta, não onde foi criada, mas sim
o bloco de código de sua origem. Isso significa que se a declararmos dentro de um
if(), switch() ou for(), ela será “enxergada” apenas dentro desta parte do código,
dentro deste escopo específico.


            function returnCar() {
            let car = 'Land Rover';
            if (car === 'Land Rover') {
            let car = 'Ferrari';
            console.log('Dentro do if: ' + car);
            }
            console.log('Fora do if: ' + car);
            }

Const: Funciona exatamente como um let, porém, sua grande diferença é que esta é
uma constante, ou seja, em momento algum pode ser alterar o valor desta const
após ter sido iniciado pelo programa.

## 4. O que é destructuring e para quais propósitos pode ser utilizado?

Destructuring é basicamente quebrar uma estrutura complexa em partes
mais simples. Por estrutura complexa, na maioria das vezes podemos
considerar como sendo um array ou um objeto.
O destructuring pode ser usado tanto para declarar variáveis quanto para
atribuir valores a variáveis.


            const resposta = {
            usuario: 'Claudiney,
            canal: 'whatsapp',
            felicidade: 80.34,
            tristeza: 1.43,
            euforia: 60.32,
            };
            const { usuario, felicidade, tristeza, euforia } = resposta;
            console.log('Olá, meu nome é ' + usuario);

            console.log('A probabilidade de felicidade no texto é de: ' + felicidade);
            console.log('A probabilidade de tristeza no texto é de: ' + tristeza);
            console.log('A probabilidade de euforia no texto é de: ' + euforia);


## 5. O que é o DOM?

O Modelo de Objeto de Documento (DOM) é uma interface de
programação para documentos HTML, XML e SVG . Ele fornece uma
representação estruturada do documento como uma árvore. O DOM define
métodos que permitem acesso à árvore, para que eles possam alterar a
estrutura, estilo e conteúdo do documento. O DOM fornece uma
representação do documento como um grupo estruturado de nós e objetos,
possuindo várias propriedades e métodos. Os nós também podem ter
manipuladores de eventos que lhe são inerentes, e uma vez que um evento é
acionado, os manipuladores de eventos são executados. Essencialmente, ele
conecta páginas web a scripts ou linguagens de programação.

<img src="https://miro.medium.com/max/740/1*Uedjd1Z-EMdhPgqYLlAjow.png" alt="Imagem de Estruturação DOM"/>


## 6. Quais problemas o JavaScript assíncrono soluciona?

O objetivo dessas funções é facilitar ainda mais o uso de promises. Uma
função assíncrona consiste em criarmos uma função “normal”, mas que
ganhará como que “superpoderes”, tornando-se uma função capaz de
trabalhar com código assíncrono.Sendo assim,JavaScript Assíncrono vem
solucionar os problemas dos códigos serem de forma síncrona, que são
aqueles que ocorrem em sequência, uma instrução após a outra.

## 7. Para que servem os comandos async e await?

Async. Essa palavra pode ser usada ao criar uma função convencional. Quando
adicionamos esse identificador na criação desta função, nós definimos que ela será uma
função assíncrona, e o melhor, retornará uma promisse. Quando usarmos a expressão
return estaremos, na realidade, resolvendo uma promisse.
Await: Essa palavra será usada com o objetivo de esperar a resolução de uma função
assíncrona. Se houver uma série de funções assíncronas, a expressão await definirá
que o código só terá sequência quando a função anterior for resolvida. Um detalhe muito
importante: a expressão await só será aceita em uma função que já for assíncrona, ou
seja, que possuir o identificador async em seu início.

## 8. Quais as vantagens de se usar Promises ao invés de callbacks?

Primeiramente vamos falar sobre o callbacks, um callback consiste em
encapsular a execução de uma requisição assíncrona e fornecer um
parâmetro em forma de função para ser invocado após a conclusão da
requisição e recebimento de resposta.
Já as promises tem a ideia de representar fluxos assíncronos de forma
sequência/vertical/top-down, além de favorecer o tratamento de exceções.
Uma grande vantagem de implementação de promises é que o retorno da
declaração é uma variável, o que torna o processo de encadeamento mais
simples. Ao final do then() das promises é possível retorna um valor qualquer
(objeto, array, string, etc) ou também uma outra promise.



