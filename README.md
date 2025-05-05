# :sparkles:Tutorial - Criação de Funções em JS

# :green_circle:DECLARATION

Declaration ou Declaração é a forma clássica de declarar uma função. Este tipo de função usa a palavra ``function`` para iniciar, logo após coloca-se um nome parra a função, junto ao nome adicionamos parênteses ``()``para colocar os parâmetros da função e logo após abrimos e fachamos chaves ``{}`` ( Dentro das chaves é escrito todo o código que a função irá realizar!).

## :green_circle: EXEMPLO

    function somar(a, b) {
        return a + b;
    };


## :white_check_mark: Vantagens
- Hoisting
- "Código Limpo"

## :no_entry: Desvantagens
- Hoisting (Em códigos de grande porte, gera confusão)
- Pouca Flexibilidade (Quando funções necessitam ser usadas como parâmetros)

## :green_circle: EXEMPLO | HOISTING

    console.log(somar(2, 8)); 
    function somar(a, b) {
        return a + b;
    };

    // Saída de log será 10, a função está sendo usada antes de ser declarada;
    // Ou seja o Hoisting está em funcionamento!

## :green_circle: EXEMPLO

    function oi(nome) {
        console.log(`Oi ${nome}!`);
    };
    oi("Juan");


# :yellow_circle: EXPRESSION

Expression ou Expressão é um tipo de função que pode ser armazenada em uma variável usando uma expressão, esta pode ser dividida em uma função anônima e nomeada.

## :yellow_circle: EXEMPLO | ANÔNIMA

    const somar = function(a, b) {
        return a + b;
    };

## :yellow_circle: EXEMPLO | NOMEADA

    const somar = function somar(a, b) {
        return a + b;
    };

## :white_check_mark: Vantagens
- Anti-Hoisting
- Ideal para ser usada dentro de outras funções

## :no_entry: Desvantagens
- Anti-Hoisting (Antes de usar deve ser declarada, ruim para código de pequeno porte!)
- Sintaxe Verbosa 

## :yellow_circle: EXEMPLO | ANTI-HOISTING

    cumprimentar("Nicolas");

    const cumprimentar = function(nome) {
        console.log(`Oi, ${nome}!`);
    };

    // Na primeira linha o código irá apresentar um erro;
    // Pois esta sendo usada antes de ser criada.

# :red_circle: ARROW

Arrow Function permitem a escrita de uma Expression de sintaxe pequena e simples. Não é preciso a palavra ``function`` também não é necessario a palavra ``return`` e chaves ``{}``.

## :white_check_mark: Vantagens
- Sintaxe Simples e curta
- ``this`` é herdado
- Ideal para manipulação de Arrays (map, reduce e filter)

## :no_entry: Desvantagens
- Não adequada para definir métodos de objetos
- Menos legivel em funções de grande porte

## :red_circle: EXEMPLO | SYNTAX

#### EXPRESSION:

    var multi = function(a, b) {
        return a * b;
    };

#### ARROW:
    const multi = (a, b) => a * b;

## :red_circle: EXEMPLO

    const dobrar = (num) => num * 2;

    console.log(dobrar(5)); 
    console.log(dobrar(12));

## :red_circle: EXEMPLO

    const dizerOi = () => console.log('Oi!');
    dizerOi(); 
