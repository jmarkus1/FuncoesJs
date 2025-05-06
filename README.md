# FuncoesJs
Declaration, Expression e Arrow. Aprenda a definir e criar essas funções em Javascript.
## Função Declaration
Também conhecida como **declaração de função,** é o jeito mais básico de definir funções em javascript,
toda função de declaração começa com uma palavra obrigatória *function*, em seguida pelo nome da função,
que também é obrigatório e uma lista de parâmetros, estes já são opcionais e são separados por vírgula
e vem dentro dos parênteses **( )** que também são obrigatórios, e o último passo será as chaves **{ }**
também sendo obrigatórias que são o corpo da função.

```javascript
function name () {}
//function (palavra resrvada) name (nome da função)
```
Essa estrutura é a mais simples, porém obrigatória para as declarações de funções. Como vimos acima
também podemos definnir parâmetros apcionais separados por vírgula:

```javascript
function name (parametro1, parametro2) {}
//function (palavra reservada) name (nome da função) parametro1 (primeiro parâmetro) parametro2 (segundo parâmetro)
```
### Vantagens de usar a função Declaration
✅ Pode ser chamada em qualquer lugar, até antes de ser declarada.  
✅ É mais fácil de compreeder já que é uma forma mais clássica e simples de fazer funções.  
✅ É melhor usada quando você quer uma função tradicional que possa ser usada em qualquer parte do código.
### Desvantagens de usar a função Declaration
❌ Ocupa mais espaço no código pois não é tão compacto.  
❌ Pode ser chamado acidentalmente antes de ser declarado o que pode causar problemas no código.  

### Exemplos de código da função Declaration
1° exemplo: **Função que soma dois números:**
```javascript
function soma (a,b) {
  return a + b;
}
console.log (soma(2,3));
```
2° exemplo: **Função que verifica se um número é par**
```javascript
function par (numero) {
  return numero % 2 === 0;
}
console.log (par(4));
```
3° exemplo: **Função que faz um cumpriment o usuário**
```javascript
function saudacao (nome) {
  return "Olá," + nome + "!";
}
console.log (saudacao("Maria"));
```
## Função Expression
A função expression tem grandes semelhanças com a declaration, a diferença é que uma função de expressão
pode ser lidada como uma expressão qualquer em javascript.  
Exemplo:
```javascript
const nome = "Jefferson"
```
Nesse exemplo foi criado uma expressão onde definimos uma variável chamada *nome* e atribuímos uma
*string* para ela.   
Utilizando as funções de expressão, podemos criar algo semelhante.
```javascript
const ola = function () {
  console.log("Olá")
}
ola()
```
Podemos observar a grande semelhnça com a função declaration uma das pequenas diferenças é que está
sendo atribuído a uma variável, onde não definimos o nome da função e sim o nome da variável que irá fazer
referência a mesma.
```javascript
const nome = function(parametro1, parametro2) {}
//const (palavra reservada) name (nome da variável) function (palavra reservada) parametro1 (1° parâmetro) parametro2 (2° parâmetro)
```
Atribuir uma função à uma variável pode ser bastante útil, por exemplo: Assim podemos definir a função exatamente
onde ela precisa ser chamada, ou seja definimos a função apenas onde precisamos dela, isso pode tornar
nosso código mais simples de entnder em alguns momentos.
### Vantagens de usar a função Expression
✅ É útil para passar funções como argumentos, já que pode ser atribuída a variáveis.   
✅ Só pode ser usada depois de ser declarada evitanndo erros, pois não sofre hoisting.   
✅ É melhor utilizado quando você precisa de uma função mais flexível, como em callbacks ou funções condicionais.
### Desvantagens de usar a função Expression
❌ Não pode ser chamado antes de ser criada.   
❌ Se for anônima, dificulta a depuração (aparece como *anonymous* em mensagens de erro).
### Exemplos de código para função Expression
1° exemplo: **Função que multiplica dois números**
```javascript
const multiplicacao = function (a,b) {
  return a*b;
};
console.log(multiplicacao(2,3));
```
2° exemplo: **Função que verifica se o número é positivo**
```javascript
const positivo = function(numero) {
  return numero > 0;
};
console.log(positivo(-5));
```
3° exemplo: **Função que retorna o dobro de um número**
```javascript
const dobro = function(num) {
  return num*2;
};
console.log(dobro(5));
```
## Função Arrow
Já que usamos bastante funções, nada melhor que criar atalhos e sintaxes menos verbosas. Pois esse 
é um dos motivos da criação das funções flecha é facilitar a criação e a utilização de funções em
javascript, já que elas permitem a criação de funções de forma resumida. Ou seja as arrow funções são
simplificações para as funcões expression.
```javascript
const name = (parametro1, parametro2) => {}
//const (palavra reservada) name (nome da variável) parametro1 (1° parâmetro) parametro2 (2° parâmetro) => (arrow símbolo)
```
Imagine a seguinte função de expressão:
```javascript
const numaleatorio = function () {
  return Math.random()
}
```
Veja que foi escrito bastante coisa, apenas para criar uma função que devolve um número aleatório
Agora veja a seguir a mesma função porém em formato de flecha.
```javascript
const numaleatorio = () => {
  return Math.random()
}
```
Até então não mudou nada apenas foi removido a palavra reservada **function** e foi adicionado um sinal de seta.   
Podemos fazer melhorias, o primeiro mexendo no **return,** repare que a função possui apenas uma linha como
conteúdo.
```javascript
const numaleatorio = () => Math.random()
```
Podemos observar que não foi removido apenas a palavra reservada **retun** como também as chaves. Ou seja:   
- Caso o corpo da função arrow tenha apenas uma linha. Vamos poder ommitir a declaração das chaves.
- Também não precisamos utilizar o **return** já que é apenas uma linha de código será executada automaticamente.
## Vantagens de usar a Função Arrow
✅ Sintaxe muito curta (perfeita para funções de linha única).   
✅ Não bagunça o **this** pois herda o contexto do código ao redor.   
✅ Melhor usado para funções rápidas, como em **map, filter** ou quando quer se evitar problemas com **this**.
## Desvantagens de usar a função Arrow
❌ Não pode ser usada como construtor.   
❌ Não tem **arguments** (precisa usar ...rest se quiser parâmetros de variáveis).
## Exemplos de códigos para função Arrow
1° exemplo: **Função que subtrai dois números**
```javascript
const subtracao = (a,b) => a - b;
console.log(subtracao(5,2));
```
2° exemplo: **Função que verifica se um número é maior que 10**
```javascript
const maiorque10 = numero => numero > 10;
console.log(maiorque10(15));
```
3° exemplo: **Função que retorna uma mensagem personalizada**
```javascript
const mensagem = nome => "Seja bem-vindo, ${nome}
console.log(mesagem("Carlos"));
```

[Referências: clique aqui](https://blog.matheuscastiglioni.com.br/definindo-funcoes-em-javascript/)




  


 
