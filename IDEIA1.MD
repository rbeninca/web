# Roteiro de aula — Introdução ao JavaScript

**Curso:** Técnico em Informática / Desenvolvimento de Sistemas
**Tema:** Fundamentos de JavaScript
**Carga sugerida:** 4 horas
**Pré-requisitos:** HTML básico e noções de lógica de programação
**Objetivo geral:** apresentar a origem, importância e principais recursos da linguagem JavaScript, conduzindo os alunos dos conceitos iniciais até pequenos programas com variáveis, tipos, seleção, repetição e funções.

---

## 1. Abertura da aula

### Objetivos da aula

Ao final da aula, o estudante deverá ser capaz de:

* explicar, de forma geral, o que é JavaScript;
* compreender por que JavaScript se tornou uma linguagem essencial na Web;
* declarar variáveis usando `let`, `const` e, historicamente, `var`;
* identificar tipos de dados básicos;
* usar estruturas de seleção com `if`, `else` e `switch`;
* usar estruturas de repetição com `for`, `while` e `do while`;
* criar funções simples;
* resolver pequenos problemas usando JavaScript.

---

# Parte 1 — História, curiosidades e motivação

## 1.1 O contexto da Web antes do JavaScript

No início da Web, as páginas eram essencialmente **documentos estáticos**. O navegador recebia HTML do servidor e apenas exibia aquele conteúdo.

Exemplo de página inicial da Web:

```html
<h1>Bem-vindo</h1>
<p>Esta é uma página estática.</p>
```

Não havia, de forma simples, interação no navegador como:

* validar um formulário antes de enviar;
* mostrar ou esconder elementos;
* criar menus interativos;
* alterar conteúdo sem recarregar a página;
* reagir imediatamente a cliques, teclas ou movimentos do usuário.

A Web precisava de uma linguagem que rodasse **dentro do navegador**.

---

## 1.2 Criação do JavaScript

JavaScript foi criado em 1995 por **Brendan Eich**, na Netscape.

Uma curiosidade importante: a primeira versão da linguagem foi criada em pouquíssimo tempo, cerca de dez dias. Isso explica algumas decisões históricas da linguagem que hoje parecem estranhas ou inconsistentes.

Inicialmente, a linguagem se chamou:

1. **Mocha**
2. depois **LiveScript**
3. depois **JavaScript**

O nome JavaScript foi uma decisão de marketing, porque a linguagem Java estava muito popular na época. Apesar do nome parecido, **JavaScript não é Java**.

Uma frase útil para os alunos:

> Java está para JavaScript assim como carro está para carpete: os nomes parecem relacionados, mas são coisas diferentes.

---

## 1.3 Por que JavaScript foi criado?

JavaScript surgiu para resolver um problema muito concreto:

> permitir que páginas Web tivessem comportamento dinâmico no lado do cliente, ou seja, dentro do navegador.

Antes, quase tudo precisava ser enviado ao servidor. Com JavaScript, parte da lógica passou a acontecer no próprio computador do usuário.

Exemplo:

```html
<button onclick="alert('Olá!')">Clique aqui</button>
```

Esse pequeno exemplo já mostra algo que HTML sozinho não fazia bem: **reagir a uma ação do usuário**.

---

## 1.4 Curiosidades importantes

### JavaScript era visto como uma linguagem “simples”

Durante muito tempo, JavaScript foi tratado como uma linguagem pequena, usada apenas para efeitos em páginas Web.

Hoje, JavaScript é usado em:

* sites;
* aplicações Web complexas;
* servidores com Node.js;
* aplicativos móveis;
* aplicações desktop;
* jogos;
* automação;
* APIs;
* sistemas embarcados em alguns contextos.

---

### JavaScript roda no navegador

Todo navegador moderno possui um interpretador de JavaScript.

Exemplos:

* Chrome usa o motor V8;
* Firefox usa SpiderMonkey;
* Safari usa JavaScriptCore.

Isso significa que, para começar a programar em JavaScript, o aluno precisa de muito pouco:

* navegador;
* editor de texto;
* arquivo HTML.

---

### JavaScript é padronizado como ECMAScript

O nome “JavaScript” é muito conhecido, mas a especificação oficial da linguagem é chamada **ECMAScript**.

Por isso aparecem nomes como:

* ES5;
* ES6;
* ES2015;
* ES2020;
* ES2023.

O ES6, também chamado ES2015, foi uma versão muito importante, pois trouxe recursos como:

* `let`;
* `const`;
* arrow functions;
* classes;
* template strings;
* módulos.

---

## 1.5 Motivações para algumas decisões da linguagem

### Tipagem dinâmica

JavaScript é uma linguagem de **tipagem dinâmica**.

Isso significa que uma variável pode receber valores de tipos diferentes ao longo do programa.

```javascript
let valor = 10;
valor = "dez";
valor = true;
```

Motivação: tornar a linguagem mais simples e flexível para scripts pequenos dentro de páginas Web.

Consequência: facilita no início, mas exige cuidado em programas maiores.

---

### Conversões automáticas

JavaScript tenta converter valores automaticamente em algumas situações.

```javascript
console.log("5" + 2); // "52"
console.log("5" - 2); // 3
```

Isso existe para tornar a linguagem mais permissiva, mas pode gerar confusão.

Por isso, recomenda-se usar:

```javascript
Number("5")
String(10)
Boolean(1)
```

---

### `var`, `let` e `const`

No início, JavaScript tinha principalmente `var`.

```javascript
var nome = "Ana";
```

Com o tempo, percebeu-se que `var` poderia causar problemas por causa do seu escopo. Então surgiram `let` e `const`.

Hoje, recomenda-se:

* usar `const` quando o valor não será reatribuído;
* usar `let` quando o valor poderá mudar;
* evitar `var` em códigos novos.

---

# Parte 2 — Entrando na linguagem

## 2.1 Onde escrever JavaScript?

Há três formas principais de usar JavaScript em uma página.

### 1. Diretamente no HTML

```html
<button onclick="alert('Olá!')">Clique</button>
```

É simples, mas não é a forma mais organizada.

---

### 2. Dentro da tag `<script>`

```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemplo</title>
</head>
<body>
    <h1>Minha página</h1>

    <script>
        console.log("Olá, JavaScript!");
    </script>
</body>
</html>
```

---

### 3. Em um arquivo externo

Arquivo `index.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemplo</title>
</head>
<body>
    <h1>Minha página</h1>

    <script src="script.js"></script>
</body>
</html>
```

Arquivo `script.js`:

```javascript
console.log("Olá, JavaScript!");
```

Essa é a forma mais organizada para projetos.

---

## Exercícios — Introdução ao JavaScript

### Teóricos

**1.** Explique com suas palavras por que JavaScript foi criado.

**2.** Qual é a diferença entre JavaScript e Java? Eles são a mesma linguagem? Justifique.

### Práticos

**3.** Crie uma página HTML com um botão que mostre a mensagem `"Bem-vindo ao JavaScript!"` usando `alert`.

**4.** Crie um arquivo `script.js` separado e faça com que ele exiba no console a mensagem:

```javascript
Iniciando meus estudos em JavaScript
```

---

# Parte 3 — Variáveis

## 3.1 O que são variáveis?

Variáveis são espaços usados para armazenar valores durante a execução do programa.

Exemplo:

```javascript
let nome = "Carlos";
let idade = 18;

console.log(nome);
console.log(idade);
```

Uma variável possui:

* nome;
* valor;
* tipo do valor;
* escopo;
* possibilidade ou não de reatribuição.

---

## 3.2 `let`

Usamos `let` quando o valor da variável pode mudar.

```javascript
let contador = 0;

contador = contador + 1;

console.log(contador);
```

---

## 3.3 `const`

Usamos `const` quando a variável não deve ser reatribuída.

```javascript
const pi = 3.14159;

console.log(pi);
```

Isso não significa que o valor interno de objetos e arrays seja sempre imutável, mas, para o início da disciplina, podemos explicar assim:

> `const` impede que a variável receba outro valor.

Exemplo inválido:

```javascript
const nome = "Ana";
nome = "Maria"; // erro
```

---

## 3.4 `var`

`var` é a forma antiga de declarar variáveis.

```javascript
var cidade = "Gaspar";
```

Em códigos modernos, recomenda-se evitar `var` e usar `let` ou `const`.

---

## 3.5 Boas práticas para nomes de variáveis

Evitar:

```javascript
let x = "João";
let a = 20;
```

Preferir:

```javascript
let nomeAluno = "João";
let idadeAluno = 20;
```

Em JavaScript, é comum usar o padrão **camelCase**:

```javascript
let nomeCompleto;
let mediaFinal;
let quantidadeAlunos;
```

---

## Exercícios — Variáveis

### Teóricos

**1.** Explique a diferença entre `let`, `const` e `var`.

**2.** Por que nomes como `mediaFinal` e `quantidadeAlunos` são melhores do que nomes como `x` e `a`?

### Práticos

**3.** Crie três variáveis: `nome`, `idade` e `curso`. Depois, exiba uma frase no console com essas informações.

Exemplo de saída:

```text
Meu nome é Ana, tenho 17 anos e estudo Informática.
```

**4.** Crie uma variável chamada `contador` com valor inicial `0`. Depois, aumente seu valor três vezes e exiba o resultado final no console.

---

# Parte 4 — Tipos de dados

## 4.1 O que são tipos de dados?

Tipos de dados indicam a natureza de um valor.

Em JavaScript, os principais tipos básicos são:

* `number`;
* `string`;
* `boolean`;
* `undefined`;
* `null`;
* `object`;
* `symbol`;
* `bigint`.

Para uma primeira aula, os mais importantes são:

```javascript
let idade = 18;              // number
let nome = "Ana";            // string
let aprovado = true;         // boolean
let endereco;                // undefined
let telefone = null;         // null
```

---

## 4.2 Number

JavaScript usa o tipo `number` para inteiros e números decimais.

```javascript
let idade = 20;
let altura = 1.75;
let temperatura = -3.5;
```

Operações:

```javascript
let soma = 10 + 5;
let subtracao = 10 - 5;
let multiplicacao = 10 * 5;
let divisao = 10 / 5;
let resto = 10 % 3;
```

---

## 4.3 String

Strings representam textos.

```javascript
let nome = "Maria";
let cidade = 'Blumenau';
```

Também é possível usar template strings com crase:

```javascript
let nome = "Maria";
let idade = 18;

console.log(`Meu nome é ${nome} e tenho ${idade} anos.`);
```

---

## 4.4 Boolean

Boolean representa verdadeiro ou falso.

```javascript
let aprovado = true;
let maiorDeIdade = false;
```

Muito usado em estruturas de seleção:

```javascript
let idade = 18;
let podeVotar = idade >= 16;

console.log(podeVotar);
```

---

## 4.5 Undefined e null

`undefined` significa que uma variável foi declarada, mas ainda não recebeu valor.

```javascript
let nome;
console.log(nome); // undefined
```

`null` representa ausência intencional de valor.

```javascript
let telefone = null;
```

Uma explicação didática:

* `undefined`: o programa ainda não colocou valor ali;
* `null`: o programador colocou “vazio” de propósito.

---

## 4.6 Verificando tipos com `typeof`

```javascript
console.log(typeof 10);        // number
console.log(typeof "texto");   // string
console.log(typeof true);      // boolean
console.log(typeof undefined); // undefined
```

Curiosidade histórica:

```javascript
console.log(typeof null); // object
```

Isso é considerado uma inconsistência histórica da linguagem.

---

## Exercícios — Tipos de dados

### Teóricos

**1.** Explique a diferença entre `undefined` e `null`.

**2.** Qual será o tipo dos valores abaixo?

```javascript
let a = 10;
let b = "10";
let c = true;
let d;
```

### Práticos

**3.** Crie variáveis para armazenar:

* nome de um produto;
* preço;
* quantidade em estoque;
* se o produto está disponível.

Depois, exiba o tipo de cada variável usando `typeof`.

**4.** Crie duas variáveis numéricas, `nota1` e `nota2`. Calcule a média e exiba uma mensagem usando template string.

Exemplo:

```text
A média do aluno foi 8.5.
```

---

# Parte 5 — Estruturas de seleção

## 5.1 O que é seleção?

Estruturas de seleção permitem que o programa tome decisões.

Exemplo em linguagem natural:

> Se a média for maior ou igual a 6, o aluno está aprovado. Caso contrário, está reprovado.

Em JavaScript:

```javascript
let media = 7;

if (media >= 6) {
    console.log("Aprovado");
} else {
    console.log("Reprovado");
}
```

---

## 5.2 Operadores relacionais

```text
>   maior que
<   menor que
>=  maior ou igual
<=  menor ou igual
==  igual, com conversão
=== igual, sem conversão
!=  diferente, com conversão
!== diferente, sem conversão
```

Recomendação:

> Em JavaScript moderno, prefira `===` e `!==`.

Exemplo:

```javascript
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

---

## 5.3 `if`, `else if` e `else`

```javascript
let nota = 8;

if (nota >= 9) {
    console.log("Excelente");
} else if (nota >= 6) {
    console.log("Aprovado");
} else {
    console.log("Reprovado");
}
```

---

## 5.4 Operadores lógicos

```text
&&  E lógico
||  OU lógico
!   NÃO lógico
```

Exemplo:

```javascript
let idade = 20;
let temCarteira = true;

if (idade >= 18 && temCarteira) {
    console.log("Pode dirigir");
} else {
    console.log("Não pode dirigir");
}
```

---

## 5.5 `switch`

O `switch` é útil quando há várias possibilidades para o mesmo valor.

```javascript
let dia = 2;

switch (dia) {
    case 1:
        console.log("Domingo");
        break;
    case 2:
        console.log("Segunda-feira");
        break;
    case 3:
        console.log("Terça-feira");
        break;
    default:
        console.log("Dia inválido");
}
```

---

## Exercícios — Estruturas de seleção

### Teóricos

**1.** Explique a diferença entre `==` e `===`.

**2.** Em que situação o uso de `switch` pode ser mais organizado do que vários `if`?

### Práticos

**3.** Crie um programa que receba uma idade e exiba:

* `"Criança"` se for menor que 12;
* `"Adolescente"` se estiver entre 12 e 17;
* `"Adulto"` se for 18 ou mais.

**4.** Crie um programa que receba uma nota de 0 a 10 e exiba:

* `"Excelente"` para nota maior ou igual a 9;
* `"Bom"` para nota entre 7 e 8.9;
* `"Regular"` para nota entre 6 e 6.9;
* `"Reprovado"` para nota menor que 6.

---

# Parte 6 — Estruturas de repetição

## 6.1 O que é repetição?

Estruturas de repetição permitem executar um bloco de código várias vezes.

Exemplo:

```javascript
console.log("Aluno 1");
console.log("Aluno 2");
console.log("Aluno 3");
console.log("Aluno 4");
console.log("Aluno 5");
```

Esse código pode ser substituído por:

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(`Aluno ${i}`);
}
```

---

## 6.2 `for`

Usamos `for` quando geralmente sabemos quantas vezes queremos repetir.

```javascript
for (let i = 1; i <= 10; i++) {
    console.log(i);
}
```

Estrutura:

```javascript
for (inicialização; condição; atualização) {
    // código repetido
}
```

---

## 6.3 `while`

Usamos `while` quando a repetição depende de uma condição.

```javascript
let contador = 1;

while (contador <= 5) {
    console.log(contador);
    contador++;
}
```

---

## 6.4 `do while`

O `do while` executa o bloco pelo menos uma vez.

```javascript
let numero = 1;

do {
    console.log(numero);
    numero++;
} while (numero <= 5);
```

Diferença importante:

* `while`: testa antes de executar;
* `do while`: executa antes e testa depois.

---

## 6.5 Cuidado com loop infinito

Um loop infinito acontece quando a condição nunca se torna falsa.

Exemplo problemático:

```javascript
let i = 1;

while (i <= 10) {
    console.log(i);
}
```

O problema é que `i` nunca muda.

Correção:

```javascript
let i = 1;

while (i <= 10) {
    console.log(i);
    i++;
}
```

---

## Exercícios — Estruturas de repetição

### Teóricos

**1.** Explique a diferença entre `for`, `while` e `do while`.

**2.** O que é um loop infinito? Dê um exemplo de situação que poderia causar isso.

### Práticos

**3.** Crie um programa que exiba no console os números de 1 a 100 usando `for`.

**4.** Crie um programa que calcule a soma dos números de 1 a 50 usando uma estrutura de repetição.

Exemplo esperado:

```text
A soma é 1275
```

---

# Parte 7 — Funções

## 7.1 O que são funções?

Funções são blocos de código reutilizáveis.

Elas ajudam a organizar o programa e evitar repetição.

Exemplo sem função:

```javascript
let media1 = (8 + 7) / 2;
console.log(media1);

let media2 = (5 + 9) / 2;
console.log(media2);
```

Exemplo com função:

```javascript
function calcularMedia(nota1, nota2) {
    return (nota1 + nota2) / 2;
}

console.log(calcularMedia(8, 7));
console.log(calcularMedia(5, 9));
```

---

## 7.2 Declarando funções

```javascript
function saudacao() {
    console.log("Olá!");
}
```

Chamando a função:

```javascript
saudacao();
```

---

## 7.3 Parâmetros

Parâmetros são valores recebidos pela função.

```javascript
function saudacao(nome) {
    console.log(`Olá, ${nome}!`);
}

saudacao("Ana");
saudacao("Carlos");
```

---

## 7.4 Retorno

Uma função pode devolver um valor usando `return`.

```javascript
function somar(a, b) {
    return a + b;
}

let resultado = somar(10, 5);

console.log(resultado);
```

---

## 7.5 Função sem retorno explícito

Quando uma função não usa `return`, ela retorna `undefined`.

```javascript
function mostrarMensagem() {
    console.log("Mensagem exibida");
}

let resultado = mostrarMensagem();

console.log(resultado); // undefined
```

---

## 7.6 Arrow functions

Em JavaScript moderno, também é comum usar arrow functions.

```javascript
const somar = (a, b) => {
    return a + b;
};
```

Quando há apenas uma expressão, pode ser simplificada:

```javascript
const somar = (a, b) => a + b;
```

Para início de curso técnico, recomenda-se primeiro ensinar:

```javascript
function somar(a, b) {
    return a + b;
}
```

Depois apresentar a versão moderna com arrow function.

---

## Exercícios — Funções

### Teóricos

**1.** Explique com suas palavras por que funções ajudam a organizar um programa.

**2.** Qual é a diferença entre uma função que apenas usa `console.log` e uma função que usa `return`?

### Práticos

**3.** Crie uma função chamada `calcularMedia` que receba duas notas e retorne a média.

Depois, use essa função para mostrar se o aluno foi aprovado ou reprovado.

**4.** Crie uma função chamada `ehPar` que receba um número e retorne `true` se ele for par e `false` caso contrário.

Exemplo:

```javascript
console.log(ehPar(10)); // true
console.log(ehPar(7));  // false
```

---

# Parte 8 — Exercício integrador

## Proposta

Criar um pequeno programa em JavaScript para classificar alunos de acordo com sua média.

### Requisitos

O programa deve:

1. armazenar o nome de um aluno;
2. armazenar duas notas;
3. calcular a média usando uma função;
4. usar estrutura de seleção para verificar a situação;
5. exibir a mensagem final.

### Exemplo de código esperado

```javascript
function calcularMedia(nota1, nota2) {
    return (nota1 + nota2) / 2;
}

let nome = "Ana";
let nota1 = 8;
let nota2 = 7;

let media = calcularMedia(nota1, nota2);

if (media >= 6) {
    console.log(`${nome} foi aprovado com média ${media}.`);
} else {
    console.log(`${nome} foi reprovado com média ${media}.`);
}
```

### Extensão para alunos mais avançados

Modificar o programa para vários alunos:

```javascript
let alunos = [
    { nome: "Ana", nota1: 8, nota2: 7 },
    { nome: "Carlos", nota1: 5, nota2: 6 },
    { nome: "Maria", nota1: 9, nota2: 10 }
];

function calcularMedia(nota1, nota2) {
    return (nota1 + nota2) / 2;
}

for (let aluno of alunos) {
    let media = calcularMedia(aluno.nota1, aluno.nota2);

    if (media >= 6) {
        console.log(`${aluno.nome} aprovado com média ${media}.`);
    } else {
        console.log(`${aluno.nome} reprovado com média ${media}.`);
    }
}
```

---

# Parte 9 — Sugestão de organização da aula

## Primeiro momento — 40 minutos

* História da Web.
* Surgimento do JavaScript.
* Diferença entre Java e JavaScript.
* Curiosidades.
* Onde JavaScript roda.
* Primeiro `alert` e primeiro `console.log`.

## Segundo momento — 50 minutos

* Variáveis.
* `let`, `const` e `var`.
* Tipos de dados.
* `typeof`.
* Exercícios de variáveis e tipos.

## Terceiro momento — 50 minutos

* Estruturas de seleção.
* Operadores relacionais.
* Operadores lógicos.
* `if`, `else if`, `else`.
* `switch`.
* Exercícios de seleção.

## Quarto momento — 50 minutos

* Estruturas de repetição.
* `for`.
* `while`.
* `do while`.
* Loop infinito.
* Exercícios de repetição.

## Quinto momento — 50 minutos

* Funções.
* Parâmetros.
* Retorno.
* Arrow functions.
* Exercício integrador.

---

# Parte 10 — Lista consolidada de exercícios

## Introdução ao JavaScript

### Teóricos

1. Explique por que JavaScript foi criado.
2. Explique a diferença entre Java e JavaScript.

### Práticos

3. Crie uma página com botão que exiba uma mensagem usando `alert`.
4. Crie um arquivo `script.js` externo e exiba uma mensagem no console.

---

## Variáveis

### Teóricos

1. Diferencie `let`, `const` e `var`.
2. Explique a importância de nomes descritivos para variáveis.

### Práticos

3. Crie variáveis `nome`, `idade` e `curso` e exiba uma frase no console.
4. Crie um contador, incremente três vezes e exiba o valor final.

---

## Tipos de dados

### Teóricos

1. Diferencie `undefined` e `null`.
2. Identifique os tipos de quatro variáveis fornecidas.

### Práticos

3. Crie variáveis de produto e mostre seus tipos com `typeof`.
4. Calcule a média de duas notas e exiba usando template string.

---

## Estruturas de seleção

### Teóricos

1. Explique a diferença entre `==` e `===`.
2. Explique quando usar `switch`.

### Práticos

3. Classifique uma pessoa como criança, adolescente ou adulto.
4. Classifique uma nota como excelente, bom, regular ou reprovado.

---

## Estruturas de repetição

### Teóricos

1. Diferencie `for`, `while` e `do while`.
2. Explique o que é loop infinito.

### Práticos

3. Exiba os números de 1 a 100.
4. Calcule a soma dos números de 1 a 50.

---

## Funções

### Teóricos

1. Explique por que funções ajudam na organização do código.
2. Diferencie uma função com `console.log` de uma função com `return`.

### Práticos

3. Crie uma função `calcularMedia`.
4. Crie uma função `ehPar`.

---

# Fechamento da aula

Ao final, pode-se reforçar a ideia central:

> JavaScript começou como uma linguagem simples para dar vida às páginas Web, mas evoluiu para uma das linguagens mais usadas do mundo. Entender bem variáveis, tipos, seleção, repetição e funções é a base para depois trabalhar com DOM, eventos, formulários, APIs, Node.js e frameworks modernos.

Sugestão de próxima aula:

* DOM;
* eventos;
* manipulação de elementos HTML;
* leitura de campos de formulário;
* alteração de conteúdo da página com JavaScript.
