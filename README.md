### Estudos JavaScript

Neste repositório deixarei por escrito algumas questões teóricas e helps sobre Javascript 

### CSS 
- [Comentários](#comentarios)


##

#### <a name="comentarios"></a> Comentários

Para comentar seu código no Javascript, pode se usar // antes da linha, para definir aquela linha inteira, para comentar mais de uma linha, pode se usar um /* no começo do comentário e um */ no final. Comentários não são executados, mas são mostrados para quem visualiza o código.

##

#### <a name="tipos-de-dados"></a> Tipos de Dados

Conforme o ECMAScript Standard (o padrão do orgão que padroniza o JavaScript) temos 9 tipos de dados organizados em 4 categorias: Primitive, Primitive Value, Structural e Structural Primitive. 

Os primitivos são: String, Number, Boolean, Undefined, Symbol, BigInt. 
Os estruturais são: Object e Function. Além destes, temos o primitivo estrutural que consiste apenas no dado null

- String

    O tipo de dados String consiste em uma cadeia de caracteres, ou seja, textos. Para denotar string no JavaScript são usados aspas duplas ( " " ), aspas simples ( ' ' ) e template literals ou template strings ( ), template literals permitem textos multilinhas e expressões de linguagem com os caracteres ${ }, por exemplo: console.log(A soma de duas unidades é ${1+1}), já as outras não, por exemplo: console.log("Isso é um texto").

- Number

    No JavaScript temos 4 tipos de números, os inteiros (por exemplo: 13), os reais ou float (por exemplo: 83.1), o Not a Number (NaN) e o infinito (Infinity).

- Boolean

    No JavaScript, um dado boolean pode ter apenas 2 valores, verdadeiro (true) e falso (false).

- Undefined vs null

    No JavaScript temos o tipo de dados Undefined, que representa valores indefinidos, e o tipo de dados null, que são muitas vezes confundidos. A diferença dos dois é que null é considerado como um objeto vazio, ou seja, algo indefinido não existe, já algo null existe mas não tem valor algum.

- Object

    O tipo de dado Object é estrutural, contendo atributos, ou propriedades, e métodos, ou funcionalidades. Um objeto é denotado com os caracteres { }, atributos e métodos com nome: valor . Por exemplo { nome: "João", idade: 20 }.

- Array

    O tipo de dados Array, ou vetor, também é estrutural, e consiste em uma lista de dados agrupados, um Array é denotado com os caracteres [ ] , por exemplo: [ "Leite", "Ovos", "Manteiga", 1, 2 ].

##

#### <a name="variaveis"></a> Variáveis

Para entender variáveis podemos pensar nelas como nomes simbólicos para algum valor, atalhos de código ou identificadores. Para criar uma variável, podemos usar uma das palavras reservadas: var, let e const, por exemplo: var clima = "quente", onde var é a palavra que simboliza a criação da variável, clima é o nome da variável, o sinal de igual denota que a variável está recebendo um valor e "quente" é a string que está sendo recebida. As variáveis declaradas com "var" e "let" podem ter seu valor mudado, já a const não.


- Scope e var

    O Scope ou Escopo determina a visibilidade de uma variável em um código, e para entender scope precisamos primeiramente entender block statement, que é o código presente dentro de chaves. O escopo do var é global, ou seja, uma variável declarada com var poderá ser usada em todo o código.

- Scope let e const

    Diferentemente de var, const e let são variáveis com escopo local, ou seja, só são visíveis no escopo onde foram criadas e em escopos interiores ao de criação. Em uma variável let, porém, pode-se alterar o valor em um escopo e o valor irá persistir no escopo de criação.

- Nomeando variáveis

    Para nomearmos variáveis corretamente e de um jeito inteligente, precisamos saber de algumas coisas, como: JavaScript é case-sensitive (sensível à letras maiúsculas e minúsculas) e aceita a cadeia de caracteres Unicode, podendo receber acentuações. Em um nome de variável em JS você pode: Iniciar com caracteres especiais, iniciar com letras e colocar acentos, lembrando sempre que letras maiúsculas e minúsculas fazem a diferença. Em contraste, você não pode: Iniciar com números e colocar espaços vazios. Idealmente você deve colocar nomes significativos, que fazem sentido na aplicação, explicando o que a variável é, usando camel case, onde a primeira palavra de uma frase é toda minúscula, e as subsequentes não se separam por espaço e tem a primeira letra maiúscula, por exemplo: oNomeDessaVariável, e usar nomes em inglês.

- Agrupando declarações

    É possível agrupar diversas declarações de variáveis em JavaScript usando let, const ou var e colocando uma vírgula entre os nomes das variáveis a serem criadas, por exemplo: let name, age, isStudent. Para mostrar mais de uma variável no console.log também é possível usando vírgula, por exemplo: console.log(name, age, isStudent).


- Concatenando e interpolando variáveis

    É possível concatenar strings com o operador +, por exemplo: console.log('o ' + name + ' tem ' + age + ' anos.') desta maneira as variáveis serão convertidas em texto e o que será mostrado será um texto com o nome e a idade que foram estabelecidas no código. Uma outra maneira de escrever um texto com variáveis é por meio da interpolação com template literals, usando crase para o texto e ${} para denotar uma variável, por exemplo console.log(O ${name} tem ${age} anos.) o resultado deste comando será o mesmo texto do anterior.

    ```javascript
    //Concatenando
    console.log('o ' + name + ' tem ' + age + ' anos.')

    //Interpolando
    console.log('o ${name} tem ${age} anos')
    ```

- Objects

    Para criarmos um objeto utilizamos as chaves envolvendo as propriedades, que são atribuídas com dois pontos, por exemplo: const person = { name: 'John', age: 20 }, para acessar essas propriedades usamos o ".", por exemplo: console.log(person.name).

- Arrays

    Para criarmos um vetor utilizamos [ ] envolvendo os valores, por exemplo: const animals = [ "Lion", "Monkey" ], para acessar esses valores usamos a posição do valor no vetor, começando por 0, por exemplo: console.log(animals[0]). Para descobrirmos o número de posições de um vetor qualquer, podemos utilizar a propriedade length, por exemplo: animals.length.

##

#### <a name="exercicios"></a> Exercícios

 ```javascript

//Declare uma variável de nome weight
var weight

// Que tipo de dado é a variável weight?
console.log(typeof weight);

//Declare uma variável e atribua valores para cada um dos dados: *name: string, * age: number(integer), * stars: number (float), * isSubscribed: boolean

var name = "Leticia"
var age = 26
var stars = 49.9
var isSubscribed = true

//A variável student abaixo é de que tipo de dados?

let student = {}
console.log(typeof student);

//Atribua ao objeto estudante as variaveis *name: string, * age: number(integer), * weight: number (float), * isSubscribed: boolean

let student = {
   name: "Leticia",
   age: 26,
   weight: 9.8,
   isSubscribed: true
}

console.log(student)

//Mostre no console a seguinde mensagem: <name> de idade <age> pesa <weight> kg

console.log('${student.name} de idade ${student.age} pesa ${student.weight} kg');

//Declare uma variável do tipo Array, de nome students e atribua a ela nenhum valor, ou seja, somente o array vazio

let students = []

//retribua o valor para a variável acima, colocando dentro dela o objeto student

students = [
  student
]

console.log(students)

//coloque no console o valor da posição zero do array acima

console.log(students[0])

//crie um novo student e coloque na posição 1 do array students

let john = {
   name: "John",
   age: 34,
   weight: 74.8,
   isSubscribed: true
}

//assim
students = [
  student,
  john
]

console.log(students)

//ou

students[1] = john
console.log(students[1])

//sem rodar o código responda qual é a redposta do código abaixo e porque? após sua resposta, rode o codigo e veja o que você acertou

console.log(a)
var a = 1

//Resposta é undefined
```

##

#### <a name="funcoes"></a> Funções

Funções são tipos de dados estruturais, que são declarados dessa forma: function nomeFunção() { código à cer executado } e para executar a função, usa-se: nomeFunção(). Uma função é importante para o agrupamento e reutilização de código.

##

#### <a name="argumentos-parametros"></a>Argumentos e parâmetros

Também é possível declarar funções dentro de variáveis, desta maneira: const variavel = function() {}. Uma parte importante de funções são os parâmetros, que são similares variáveis que funcionam para colocar dados em funções, eles são declarados junto à declaração da função e quando a função for executada, os valores dos argumentos são colocados dentro dos parênteses.

##

#### <a name="retornando-valores-dentro-da-funcao"></a> Retornando valores dentro da função

Para passar valores de dentro da função para o resto do código, usa-se a palavra reservada return seguida do valor à ser retornado, parando assim a execução da função e mandando o valor para onde a função foi chamada.

##

#### <a name="function-hoisting"></a> Function Hoisting

O JavaScript possui function hoisting, permitindo que uma função seja declarada depois de ser utilizada, pois faz algo similar a elevar no código declarações de funções. Porém isso não acontece dentro de variáveis.

##

#### <a name="arrow-function"></a> Arrow function

Também podemos escrever funções expression de uma maneira mais compacta, desta maneira: () => { código a ser executado }, chamada de Arrow Function.

##

#### <a name="callback-function"></a>Callback function

Uma callback function é uma função que está sendo passada para outra função como parâmetro.

##

#### <a name="function-construtoras"></a>Funções construtoras

Funções construtoras são utilizadas para criar novos objetos e geralmente tem a sua primeira letra maiúscula, todos com as mesmas características que são criadas na função, usando a palavra reservada this para se referir ao objeto sendo criado, por exemplo:

    ```javascript
    function Person(name) {
        this.name = name
        this.walk() = function() {
            return this.name + "está andando")
        }
    }
    const mayk = new Person("Mayk")
    const joao = new Person("João")
    ```

##

#### <a name="prototype"></a>Prototype

O JavaScript possui uma característica chamada Prototype, que é uma série de funcionalidades e atributos que já existem nativamente em diversos tipos de dados, que são lidados como objetos.

##

#### <a name="type-conversion-coersion"></a>Type conversion coersion

Type conversion se trata de uma conversão de tipo feita pelo dev, explicitamente, e pode ser feita de diversas maneiras, por exemplo com o método Number(), já type coersion é uma mudança de tipos feita pelo próprio JavaScript, implicitamente, por exemplo quando você tenta somar um número na forma string com um número do tipo número.

- É possível transformar números em formato de string através do método Number() e números em formato number em string usando o método String().


##

#### <a name="manipulando-dados"></a>Manipulando Dados

- Contando caracteres e digitos

    Para contar a quantidade de caracteres em uma string é possível usar o método length(), também é possível contar a quantidade de algarismos em um número transformando o número em string e usando o mesmo método.

- Casas decimais

    Para determinar uma quantia de casas decimais de um número pode-se usar o método toFixed() colocando como argumento quantas casas decimais o número terá. Para mudar a formatação do número de separado por ponto para separado por vírgula é possível usar o método replace(".", ","). O resultado final será do tipo string, e a conversão para o tipo número não será possível por que a vírgula não é considerada parte de um número.

- Maiúsculas e minúsculas

    Para transformar uma string em letras maiúsculas pode-se usar o método toUpperCase(), e ao contrário, também é possível usar o toLowerCase() para transformar uma string em todas letras minúsculas.

- Separando strings

    Para separar um texto por espaços, pode-se usar o método split(" "), que transforma o texto em um array de strings baseado no argumento, que no caso são os espaços. Para juntar esse array é possível usar o método join('"), que juntaria essas palavras sem nenhum separador, porém colocando um argumento, no caso um underscore ( join("_") ) as palavras são juntadas com o argumento de separador.

- Encontrando palavras em frases

    Para verificar se um texto possui uma palavra específica, podemos usar o método includes(), passando como argumento a palavra a ser verificada, que retorna um valor true se encontrar a palavra, e falso se não, lembrando sempre que o método é case sensitive.

- Criando array com construtor

    Para criar um array com um método construtor, usa-se new Array(args), passando como argumento o tamanho deste vetor ou os valores, por exemplo: const array = new Array("a", "b", "c").

- Elementos do Array

    Para contar a quantidade de elementos em um array pode-se usar o método length.

- Strings para arrays

    Para transformar uma string em um array, pode-se usar o objeto Array com o método from(), passando como argumento a string a ser transformada em array. Por exemplo console.log(Array.from("developer").

- Manipulando arrays

    Existem várias maneiras de manipular arrays, como: o método push(), que adiciona um elemento no final do array, o método unshift(), que adiciona um elemento no começo do array, o método pop(), que retira um elemento do final do array, o método shift(), que retira um elemento do começo do array, o método slice(), que recebe como argumentos a posição de início e a posição do fim da parte que você quer selecionar, e retorna os valores destas posições, o método splice(), que recebe como argumentos a posição de início e a quantidade de elementos que você quer remover e o método indexOff(), que encontra o index do valor que recebe como argumento em um array.
    
    ```javascript
    let techs = ["html", "css", "js"]

    //adicionar um item no fim
    techs.push("nodejs")

    //adicionar no começo
    techs.unshift("sql")

    //Remover no fim
    techs.pop()

    //remover no começo
    techs.shift()

    //pegar somente alguns elementos do array
    console.log(techs.slice(1,3))

    //remover 1 ou mais items em qualquer posição do array
    techs.slice(1,1)

    //encontrar a posição de um elemento no array
    let index = techs.indexOf('css')
    techs.slice(index,1)

    console.log(techs)
    ```







































