# Aula 2 — JavaScript no navegador: DOM, eventos, entrada de dados e pequenos programas

**Curso:** Programação para Internet / Curso Técnico
**Tema:** JavaScript aplicado à interação com páginas HTML
**Carga sugerida:** 4 horas
**Pré-requisitos:** conteúdo da Aula 1: história do JavaScript, variáveis, tipos de dados, estruturas de seleção, repetição e funções básicas.

---

## 1. Contexto da Aula 2

Na primeira aula, foram apresentados os fundamentos da linguagem JavaScript:

* contexto histórico da linguagem;
* motivação para sua criação;
* execução no navegador;
* variáveis com `let`, `const` e `var`;
* tipos de dados;
* operadores;
* estruturas de seleção;
* estruturas de repetição;
* funções.

A Aula 2 deve avançar da linguagem isolada para o uso do JavaScript dentro de páginas HTML, explorando a interação com o usuário e a manipulação dos elementos da página.

A ideia central da aula é mostrar que JavaScript não serve apenas para calcular valores no console, mas também para modificar a página, responder a eventos, ler campos de formulário, alterar estilos e produzir pequenos aplicativos Web.

---

# 2. Objetivos da aula

Ao final da aula, o estudante deverá ser capaz de:

* compreender o papel do DOM em uma página Web;
* acessar elementos HTML usando `document.getElementById()`;
* alterar textos e conteúdos usando `innerText`, `innerHTML` e `value`;
* usar `alert`, `prompt` e `console.log` de forma didática;
* associar funções JavaScript a eventos de clique, teclado, foco, mudança e mouse;
* ler dados digitados pelo usuário em campos `<input>`;
* converter valores de texto para número usando `parseInt`, `parseFloat` e `Number`;
* validar campos antes de processar dados;
* usar `Math.random()` para gerar números aleatórios;
* usar arrays para armazenar informações temporárias;
* construir pequenos programas interativos em HTML, CSS e JavaScript.

---

# 3. Análise dos exercícios enviados

A lista original contém exercícios muito bons, mas mistura conteúdos de níveis diferentes. Alguns exercícios são introdutórios e combinam diretamente com a Aula 2; outros exigem mais maturidade e podem ser deixados como desafio ou continuação.

## 3.1 Exercícios mais adequados para a Aula 2

Os exercícios mais adequados para esta aula são:

* **Questão 1 — O que é JavaScript?**
  Boa para revisar a Aula 1 e introduzir `document`, `console` e `alert`.

* **Questão 2 — Tipos de variáveis e operadores**
  Boa para reforçar tipos de dados, `typeof`, conversões automáticas e escrita no DOM.

* **Questão 3 — prompt e alert**
  Boa para apresentar entrada de dados simples.

* **Questão 4 — Cálculo de IMC**
  Excelente exercício integrador com inputs, conversão numérica, função, seleção e alteração do DOM.

* **Questão 5 — Gerador de números aleatórios**
  Boa para introduzir `Math.random()`, eventos e armazenamento em array.

* **Questão 8 — Mudança de cor de fundo com clique**
  Boa para trabalhar eventos, estilos e manipulação visual da página.

* **Questão 11 — Explorando eventos**
  Excelente para sistematizar eventos como `click`, `keydown`, `focus`, `blur`, `mouseover`, `mouseout` e `change`.

* **Questão 14 — Captura de teclas do teclado**
  Boa continuação da Questão 11, com foco em eventos de teclado.

---

## 3.2 Exercícios que podem ficar como desafio ou Aula 3

Alguns exercícios são interessantes, mas podem exigir mais tempo ou novos conceitos:

* **Questão 6 — Números primos em intervalo**
  Exige boa compreensão de laços, funções e lógica matemática. Pode ser usado como desafio.

* **Questão 7 — Palíndromos**
  Envolve strings, normalização e comparação. Pode ser ótimo para uma aula posterior sobre strings.

* **Questão 9 — Alteração de cores com tecla de espaço**
  É uma boa continuação dos eventos de teclado.

* **Questão 10 — Calculadora aritmética**
  É um excelente exercício integrador, mas pode ser melhor como fechamento de bloco.

* **Questão 12 — Local Storage**
  Introduz persistência no navegador. Pode ser tema de uma aula própria ou parte final da Aula 2, se houver tempo.

* **Questão 13 — Canvas**
  É interessante, mas abre um novo tópico. Recomenda-se deixar para uma aula específica sobre APIs do navegador.

---

# 4. Proposta didática para a Aula 2

## 4.1 Tema central

**Do console para a página: criando interações com JavaScript.**

Na Aula 1, o aluno aprendeu os fundamentos da linguagem. Na Aula 2, ele deve perceber que esses fundamentos são usados para controlar uma página HTML.

---

## 4.2 Sequência sugerida da aula

## Primeiro momento — Revisão e conexão com a Aula 1

**Tempo sugerido:** 20 a 30 minutos

Retomar rapidamente:

* variáveis;
* tipos de dados;
* operadores;
* `if`;
* `for`;
* funções;
* `console.log()`.

Pergunta disparadora:

> Na Aula 1, usamos JavaScript para calcular e exibir mensagens no console. Como podemos usar JavaScript para alterar uma página HTML?

Exemplo inicial:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Aula 2</title>
</head>
<body>
    <h1 id="titulo">Título original</h1>
    <button onclick="alterarTitulo()">Alterar título</button>

    <script>
        function alterarTitulo() {
            document.getElementById("titulo").innerText = "Título alterado com JavaScript";
        }
    </script>
</body>
</html>
```

---

## Segundo momento — DOM e acesso a elementos HTML

**Tempo sugerido:** 40 minutos

Explicar que o navegador transforma o HTML em uma estrutura de objetos chamada DOM.

DOM significa **Document Object Model**.

Com JavaScript, podemos acessar e modificar elementos da página.

### Conceitos principais

```javascript
document.getElementById("titulo")
```

Acessa um elemento pelo seu `id`.

```javascript
document.getElementById("saida").innerText = "Texto novo";
```

Altera o texto visível de um elemento.

```javascript
document.getElementById("saida").innerHTML = "<strong>Texto em negrito</strong>";
```

Altera o conteúdo HTML interno de um elemento.

```javascript
let nome = document.getElementById("nome").value;
```

Lê o valor digitado em um campo de formulário.

---

## Terceiro momento — Entrada e saída de dados

**Tempo sugerido:** 40 minutos

Apresentar três formas simples de entrada e saída:

## Saída no console

```javascript
console.log("Mensagem no console");
```

## Saída em janela

```javascript
alert("Mensagem para o usuário");
```

## Entrada simples

```javascript
let nome = prompt("Digite seu nome:");
alert("Olá, " + nome);
```

## Saída no HTML

```javascript
document.getElementById("mensagem").innerText = "Olá, usuário!";
```

Destacar que `prompt` e `alert` são úteis para aprender, mas em aplicações reais é mais comum usar campos HTML.

---

## Quarto momento — Eventos

**Tempo sugerido:** 50 minutos

Explicar que eventos são ações que acontecem na página.

Exemplos:

* clique em botão;
* digitação no teclado;
* movimento do mouse;
* entrada ou saída de foco de um campo;
* mudança de valor em um `<select>`.

### Evento de clique com `onclick`

```html
<button onclick="mostrarMensagem()">Clique aqui</button>
<p id="saida"></p>

<script>
function mostrarMensagem() {
    document.getElementById("saida").innerText = "Botão clicado!";
}
</script>
```

### Evento com `addEventListener`

```html
<button id="botao">Clique aqui</button>
<p id="saida"></p>

<script>
const botao = document.getElementById("botao");

botao.addEventListener("click", function() {
    document.getElementById("saida").innerText = "Evento tratado com addEventListener";
});
</script>
```

Explicar que `onclick` é mais simples para começar, mas `addEventListener` é mais organizado e flexível em projetos maiores.

---

## Quinto momento — Conversão de dados e validação

**Tempo sugerido:** 40 minutos

Mostrar que valores lidos de inputs normalmente chegam como texto.

```html
<input type="number" id="idade">
<button onclick="verificar()">Verificar</button>
<p id="resultado"></p>

<script>
function verificar() {
    let idade = document.getElementById("idade").value;
    console.log(typeof idade); // string
}
</script>
```

Mesmo usando `type="number"`, o valor lido com `.value` vem como string.

Conversão:

```javascript
let idade = Number(document.getElementById("idade").value);
```

Ou:

```javascript
let peso = parseFloat(document.getElementById("peso").value);
let quantidade = parseInt(document.getElementById("quantidade").value);
```

Validação simples:

```javascript
if (nome === "" || isNaN(peso) || isNaN(altura)) {
    alert("Preencha todos os campos corretamente.");
    return;
}
```

---

## Sexto momento — Exercício guiado: cálculo de IMC

**Tempo sugerido:** 50 minutos

Construir com os alunos o exercício de IMC, pois ele integra vários conceitos:

* leitura de inputs;
* conversão com `parseFloat`;
* validação;
* função para cálculo;
* estrutura `if / else if / else`;
* escrita no DOM;
* alteração de imagem ou estilo.

### Estrutura base

```html
<h1>Cálculo de IMC</h1>

<label>Nome:</label>
<input type="text" id="nome">

<label>Peso:</label>
<input type="number" id="peso" step="0.1">

<label>Altura:</label>
<input type="number" id="altura" step="0.01">

<button onclick="calcularIMC()">Calcular</button>

<p id="resultadoIMC"></p>
<p id="classificacao"></p>
```

### JavaScript base

```javascript
function calcularIMC() {
    let nome = document.getElementById("nome").value;
    let peso = parseFloat(document.getElementById("peso").value);
    let altura = parseFloat(document.getElementById("altura").value);

    if (nome === "" || isNaN(peso) || isNaN(altura) || altura <= 0) {
        alert("Preencha todos os campos corretamente.");
        return;
    }

    let imc = peso / (altura * altura);
    let textoClassificacao = "";

    if (imc < 18.5) {
        textoClassificacao = "Abaixo do peso";
    } else if (imc < 24.9) {
        textoClassificacao = "Peso normal";
    } else if (imc < 29.9) {
        textoClassificacao = "Sobrepeso";
    } else if (imc < 34.9) {
        textoClassificacao = "Obesidade grau 1";
    } else if (imc < 39.9) {
        textoClassificacao = "Obesidade grau 2";
    } else {
        textoClassificacao = "Obesidade grau 3";
    }

    document.getElementById("resultadoIMC").innerText = `${nome}, seu IMC é ${imc.toFixed(2)}.`;
    document.getElementById("classificacao").innerText = `Classificação: ${textoClassificacao}`;
}
```

---

# 5. Lista de exercícios da Aula 2

## Orientações gerais

Crie uma pasta chamada:

```text
ppi1_lista_js_aula2
```

Dentro dela, crie os arquivos indicados em cada exercício.

Cada exercício deve conter:

* estrutura HTML completa;
* uso adequado de `id` nos elementos manipulados pelo JavaScript;
* código JavaScript dentro da própria página ou em arquivo externo;
* pelo menos um `console.log()` para depuração ou conferência;
* commits claros no Git;
* publicação no GitHub Pages.

Sugestão de estrutura:

```text
ppi1_lista_js_aula2/
├── index.html
├── 1.html
├── 2.html
├── 3.html
├── 4.html
├── 5.html
├── 6.html
├── 7.html
├── 8.html
├── css/
│   └── estilo.css
├── js/
│   ├── exercicio1.js
│   ├── exercicio2.js
│   └── ...
└── README.md
```

---

# Exercício 1 — Revisão: o que é JavaScript?

**Arquivo:** `1.html`

Crie um documento HTML com explicações e exemplos sobre JavaScript.

## Requisitos

A página deve conter:

1. título da aba do navegador com o texto:

```text
O que é JavaScript?
```

2. um título `<h1>` com a mesma pergunta;
3. um parágrafo explicando a motivação da criação do JavaScript;
4. um parágrafo explicando a diferença entre execução no navegador e execução no servidor;
5. um parágrafo explicando o conceito de sandbox no navegador;
6. exemplos ou explicações sobre os objetos globais:

   * `document`;
   * `console`;
   * `alert`.

## Requisitos de JavaScript

* Use `console.log()` para registrar uma mensagem no console.
* Use `alert()` para exibir uma saudação ao carregar a página.
* Exiba a hora atual em um parágrafo usando:

```javascript
document.getElementById("horaAtual").innerHTML = new Date();
```

---

# Exercício 2 — Tipos de variáveis, operadores e escrita no DOM

**Arquivo:** `2.html`

Crie uma página com um botão que, ao ser clicado, execute um script JavaScript para demonstrar tipos de dados e operações.

## Requisitos

Declarar variáveis dos seguintes tipos:

* `string`;
* `number`;
* `boolean`;
* `undefined`;
* `null`;
* `object`;
* `array`.

## A página deve mostrar

Para cada variável, exiba em um parágrafo:

* o valor;
* o tipo retornado por `typeof`.

Exemplo de ids:

```html
<p id="pstring"></p>
<p id="pnumero"></p>
<p id="pboolean"></p>
```

## Operações obrigatórias

Mostre no console e na página o resultado das operações:

```javascript
"5" + 2
"5" - 2
true + 1
false * 10
10 / "2"
```

Explique brevemente o comportamento de cada uma.

---

# Exercício 3 — Entrada simples com prompt e saída com alert

**Arquivo:** `3.html`

Crie um documento HTML que, ao ser carregado, faça as seguintes ações:

1. exiba um `prompt` perguntando o nome do usuário;
2. armazene o nome em uma variável;
3. imprima o conteúdo lido em um `alert`;
4. mostre também a saudação dentro da página usando `innerText`.

Exemplo:

```javascript
let nome = prompt("Digite seu nome:");
alert("Olá, " + nome);
document.getElementById("mensagem").innerText = "Olá, " + nome;
```

---

# Exercício 4 — Cálculo de IMC com formulário, if e DOM

**Arquivo:** `4.html`

Crie uma página para calcular o IMC de uma pessoa.

## Elementos obrigatórios no HTML

```html
<input type="text" id="nome">
<input type="number" id="peso" step="0.1">
<input type="number" id="altura" step="0.01">
<button onclick="calcularIMC()">Calcular</button>
<p id="resultadoIMC"></p>
<p id="classificacao"></p>
<img id="imgPerfil" alt="Imagem da classificação">
```

## Regras

* Verifique se os campos foram preenchidos.
* Use `parseFloat()` para peso e altura.
* Calcule o IMC com a fórmula:

```text
IMC = peso / altura²
```

* Use `toFixed(2)` para exibir o IMC com duas casas decimais.
* Use `if / else if / else` para classificar o IMC:

```text
Abaixo do peso: IMC < 18.5
Peso normal: 18.5 <= IMC < 24.9
Sobrepeso: 25 <= IMC < 29.9
Obesidade grau 1: 30 <= IMC < 34.9
Obesidade grau 2: 35 <= IMC < 39.9
Obesidade grau 3: IMC >= 40
```

## Desafio adicional

Altere a imagem exibida em `<img id="imgPerfil">` conforme a classificação.

Sugestão de nomes de arquivos:

```text
imgs/magro.png
imgs/normal.png
imgs/sobrepeso.png
imgs/obeso1.png
imgs/obeso2.png
imgs/obeso3.png
```

---

# Exercício 5 — Sorteio de números com intervalo personalizado

**Arquivo:** `5.html`

Crie uma página que gere números aleatórios com base em um intervalo informado pelo usuário.

## Elementos obrigatórios

* título `<h1>` com o texto `Sorteio de Números`;
* campo para valor mínimo;
* campo para valor máximo;
* botão com o texto `Sortear`;
* parágrafo ou div para mostrar o resultado;
* lista com os números já sorteados.

## Requisitos de JavaScript

* Implemente uma função chamada `sortear()`.
* Leia os valores mínimo e máximo dos inputs.
* Converta os valores para número.
* Valide se o mínimo é menor ou igual ao máximo.
* Gere um número aleatório inteiro dentro do intervalo.
* Mostre o número sorteado na tela.
* Armazene os números sorteados em um array.
* A cada sorteio, mostre quantas vezes cada número já apareceu.

## Sugestão

Use um array de objetos:

```javascript
let sorteados = [
    { numero: 10, quantidade: 2 },
    { numero: 25, quantidade: 1 }
];
```

---

# Exercício 6 — Mudança de cor de fundo com clique

**Arquivo:** `6.html`

Crie uma página Web com um botão que, ao ser clicado, altere a cor de fundo da página para uma cor aleatória.

## Requisitos

* Crie um botão com o texto `Alterar cor`.
* Gere uma cor aleatória em um dos formatos:

  * `#RRGGBB`;
  * `rgb()`;
  * `hsl()`.
* Altere a cor de fundo da página.
* Exiba na tela o código da cor atual.

## Desafio adicional

Copie a cor gerada para a área de transferência usando a API `navigator.clipboard.writeText()`.

---

# Exercício 7 — Explorando eventos em JavaScript

**Arquivo:** `7.html`

Use o HTML abaixo e escreva o JavaScript necessário para tornar os elementos interativos.

```html
<body>
  <button id="alertButton">Clique aqui</button>
  <input type="text" id="textInput" placeholder="Digite algo">
  <div id="hoverDiv">Passe o mouse aqui</div>
  <select id="colorSelect">
    <option value="">Escolha uma cor</option>
    <option value="blue">Azul</option>
    <option value="green">Verde</option>
    <option value="red">Vermelho</option>
  </select>
</body>
```

## Requisitos

Use JavaScript para implementar:

1. quando o botão for clicado, exibir um `alert()` com uma mensagem;
2. quando o usuário digitar no campo de texto, exibir cada tecla no console usando `keydown`;
3. ao focar o campo de texto, mudar a cor de fundo do campo para amarelo usando `focus`;
4. ao sair do campo de texto, restaurar a cor original usando `blur`;
5. quando o mouse passar sobre a `div`, mudar sua cor de fundo usando `mouseover`;
6. quando o mouse sair da `div`, restaurar a cor original usando `mouseout`;
7. ao escolher uma opção no `select`, alterar a cor de fundo da página usando `change`.

---

# Exercício 8 — Captura de teclas do teclado

**Arquivo:** `8.html`

Crie uma página HTML onde o usuário possa visualizar em tempo real as teclas que digita no teclado.

## Requisitos

A página deve conter:

```html
<h1>Captura de Teclas do Teclado</h1>
<div id="saida"></div>
```

Use JavaScript para:

* capturar cada tecla pressionada com o evento `keydown`;
* mostrar no `<div id="saida">` as teclas digitadas em sequência;
* registrar no console a tecla pressionada;
* exibir também o código da tecla usando `event.code`.

## Desafio adicional

Trate a tecla `Backspace` para apagar o último caractere exibido.

---

# 6. Exercícios extras para alunos avançados

Os exercícios abaixo podem ser usados como continuação, recuperação paralela ou desafio.

---

## Extra 1 — Números primos em um intervalo

**Arquivo:** `extra1.html`

Crie uma página que permita ao usuário descobrir todos os números primos dentro de um intervalo definido por ele.

## Requisitos

* Campo para número inicial.
* Campo para número final.
* Botão `Verificar`.
* Div para mostrar os números primos encontrados.
* Valide os limites.
* Normalize o intervalo caso o início seja maior que o fim.
* Crie uma função:

```javascript
function ehPrimo(n) {
    // implementação
}
```

---

## Extra 2 — Verificador de palíndromos

**Arquivo:** `extra2.html`

Crie uma página onde o usuário possa digitar uma palavra e verificar se ela é um palíndromo.

Exemplos:

```text
a    → é palíndromo
ab   → não é palíndromo
aba  → é palíndromo
abba → é palíndromo
```

---

## Extra 3 — Calculadora aritmética

**Arquivo:** `extra3.html`

Crie uma calculadora simples usando HTML e JavaScript.

## Requisitos

A calculadora deve realizar:

* adição;
* subtração;
* multiplicação;
* divisão.

Deve conter:

* dois campos numéricos;
* seleção da operação;
* botão para calcular;
* exibição do resultado na tela.

---

## Extra 4 — Salvando nome com Local Storage

**Arquivo:** `extra4.html`

Utilize JavaScript para salvar e recuperar um nome digitado usando `localStorage`.

HTML sugerido:

```html
<body>
  <input type="text" id="nameInput" placeholder="Digite seu nome">
  <button id="saveButton">Salvar</button>
  <p id="greeting"></p>
</body>
```

## Requisitos

* Ao clicar em salvar, grave o nome no `localStorage`.
* Ao recarregar a página, recupere o nome salvo.
* Exiba uma saudação no parágrafo.

---

# 7. Critérios de avaliação sugeridos

| Critério                                           | Peso sugerido |
| -------------------------------------------------- | ------------: |
| Estrutura correta dos arquivos HTML                |           15% |
| Uso adequado de ids e manipulação do DOM           |           20% |
| Uso correto de variáveis, tipos e conversões       |           15% |
| Uso correto de eventos                             |           20% |
| Validação de entradas                              |           10% |
| Organização do código e legibilidade               |           10% |
| Versionamento com Git e publicação no GitHub Pages |           10% |

---

# 8. Encaminhamento para a próxima aula

A próxima aula pode avançar para um dos seguintes caminhos:

## Opção A — Strings, arrays e pequenos algoritmos

Conteúdos:

* métodos de string;
* arrays;
* laços com arrays;
* palíndromos;
* números primos;
* busca e contagem.

## Opção B — Eventos e interface mais organizada

Conteúdos:

* `addEventListener` com mais profundidade;
* separação entre HTML, CSS e JS;
* validação de formulários;
* mensagens de erro no DOM;
* miniaplicações Web.

## Opção C — APIs do navegador

Conteúdos:

* `localStorage`;
* Canvas;
* Clipboard API;
* manipulação visual mais avançada.

---

# 9. Síntese da aula

A Aula 2 deve mostrar ao aluno que JavaScript ganha sentido prático quando conectado ao HTML.

A sequência recomendada é:

1. revisar fundamentos da linguagem;
2. apresentar o DOM;
3. ler e alterar elementos da página;
4. trabalhar com eventos;
5. converter e validar entradas;
6. desenvolver pequenos programas interativos.

Com isso, os alunos estarão preparados para construir páginas Web dinâmicas e para avançar posteriormente para formulários, arrays, armazenamento local, consumo de APIs e aplicações Web mais completas.
