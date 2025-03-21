# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
``a) A saída será undefined seguido de erro`` 

``Essa é a resposta correta, pois ele irá retornar undefined do console.log(x) e retornará um erro dizendo que a variável y não foi inicializada``

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

``b) Substituir if (a || b === 0) por if (a === 0 && b === 0) ``

`` Essa é a opção correta, pois agora estamos comparando as variáveis separadamente da maneira certa, com isso os parâmetros 2 e 0 serão utilizados na função de soma e retornarão corretamente``

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

``b) O código imprime 200.`` 

``O código irá imprimir 200, pois não foi colocado um break no primeiro case do switch, então ele continua até chegar na linha em que a variável preço passa a ser 200 e imprime esse valor (onde há um break).``

c) O código imprime 50.

d) O código gera um erro.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

``d) 24`` 

`` Essa é a opção correta, pois o código vai multiplicar todos os itens do array por 2, depois vai retirar os menores que 5 e somar os que sobraram. Com isso, o valor que resultou foi 24.``
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

``c) ["banana", "abacaxi", "manga", "laranja"]``

``Essa é a opção correta, pois ele vai substituir os itens nas posições 1 e 2 do array pelos que ele passou como parâmetro respectivamente.``

d) ["banana", "maçã", "uva", "abacaxi", "manga"]
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


``a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.``

``Acredito que essa seja a opção correta, pois a primeira afirmação define bem o conceito de herança e a segunda fala corretamente sobre como ela é aplicada em JS através do uso do extends (poderia melhor explicado mostrando a sintaxe completa, mas ainda sim acredito que esteja correto)`` 

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

``a) I e II são verdadeiras.``

``Acredito que essa seja a resposta correta, pois de fato a classe Funcionário herda os atributos de Pessoa e o método apresentar() está sendo sobreposto na classe estendida Funcionário. Ele só não funciona pois não foi feita nenhuma instância de nenhuma das duas classes.`` 


b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.


______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

``c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.`` 

``Acredito que essa resposta seja a correta pois de fato o conceito de polimorfismo, como por exemplo uma classe brinquedo e as classes carro e avião que herdam da mesma classe pai brinquedo, mas usam um método mover(), por exemplo, de maneiras diferentes. Mas não necessariamente a sobrecarga de métodos explica essa asserção, pois o polimorfismo não depende dela.``

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {
    soma = 0; // A variável soma não estava definida
    for (i = 0; i < numeros.length; i++) { // O correto é numeros.length ao invés de numeros.size
        soma += 2*numeros[i]; // Aqui o código não estava somando o dobro de cada número, somente armazenando o dobro do número na posição atual do loop.
    }
    return soma; // Aqui o código retorna a soma
}
console.log(somaArray([1, 2, 3, 4]));
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

``Para realizar o desconto na classe Livro que herda de Produto, basta repetir o método calcularDesconto() com o novo cálculo de desconto que automaticamente ela irá sobrescrever o método da classe pai alterando somente seu funcionamento na classe estendida.``


```javascript
// Classe base Produto
class Produto {
    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
    }
    
    calcularDesconto() {
        const desconto = this.preco * 0.1; // 10% de desconto
        return this.preco - desconto;
    }
    
    exibirInfo() {
        console.log(`Produto: ${this.nome}`);
        console.log(`Preço original: R$ ${this.preco.toFixed(2)}`);
        console.log(`Preço com desconto: R$ ${this.calcularDesconto().toFixed(2)}`);
        console.log("------------------------");
    }
}

// Classe Livro que herda de Produto
class Livro extends Produto {
    constructor(nome, preco) {
        super(nome, preco); // Chama o construtor da classe pai
    }
    
    // Sobrescreve o método calcularDesconto 
    calcularDesconto() {
        const desconto = this.preco * 0.2; // 20% de desconto 
        return this.preco - desconto;
    }
    
}

// Instanciando as classes criadas
const produto1 = new Produto("Caderno", 25.00);
produto1.exibirInfo();

const livro1 = new Livro("A Culpa é das Estrelas", 50.00);
livro1.exibirInfo();

```