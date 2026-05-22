Aqui está o roteiro completo da aula de CSS, formatado em Markdown, pronto para
ser utilizado em repositórios, plataformas de ensino ou impresso.

Roteiro de Aula — A Evolução do Estilo: Da Web "Feia" ao CSS Moderno

Curso: Análise e Desenvolvimento de Sistemas — ADS
Unidade curricular: Programação para Internet
Tema da aula: CSS (Cascading Style Sheets): Histórico, Sintaxe, Métodos e Box
Model
Carga sugerida: 4 horas
Pré-requisitos: Conhecimento básico de HTML (tags, estrutura e atributos)

1. Abertura: O Caos Pré-1996

O Problema Histórico

Antes do CSS, o HTML tentava fazer tudo. Para mudar a cor de uma fonte, usava-se
a tag <font color="red">. Se um site tivesse 100 páginas, e o cliente pedisse
para mudar o vermelho para azul, o desenvolvedor teria que abrir 100 arquivos e
alterar tag por tag.

Ponto de reflexão: "O HTML foi criado para estruturar dados científicos, não
para ser uma ferramenta de design gráfico. O CSS nasceu para salvar a sanidade
dos desenvolvedores."

Sugestão de Atividade Visual:

  - Projete o site original do Space Jam (1996) — um exemplo clássico de design
    feito puramente com tabelas e tags de fonte.
  - Mostre o CSS Zen Garden — um site onde o mesmo HTML muda completamente de
    aparência apenas trocando o arquivo CSS.

2. Parte 1 — Cronologia: A Batalha pela Padronização
A evolução do CSS reflete a necessidade de criar layouts cada vez mais complexos.

| Período | Marco | Principais Características |
| :--- | :--- | :--- |
| **1994** | **Proposta Inicial** | Håkon Wium Lie propõe o CSS no CERN. O foco é separar conteúdo (HTML) de apresentação (CSS). |
| **1996** | **CSS1** |  O W3C publica o CSS nível 1. O suporte nos navegadores era terrível. Introdução das cores, fontes e a propriedade **`float`**. O `float` permitia que o texto fluísse ao redor de imagens, mas acabou sendo "gambiarra" para criar colunas. |
| **1998** | **CSS2** | CSS nível 2. Surge o suporte a posicionamento (absolute/relative) Introdução do **`position`** (`static`, `relative`, `absolute`, `fixed`) e do **`z-index`**. Maior precisão no posicionamento de elementos sobrepostos. |
| **2000-2009** | **A Era das Trevas** | Navegadores como Internet Explorer tinham suporte parcial e cheio de bugs. Desenvolvedores criavam "hacks" (ex: `* html` para IE6) para tentar contornar as diferenças. |
| **2004-11** | **CSS2.1** | Fase de refinamento e padronização. Corrigiu inconsistências entre navegadores e consolidou as técnicas de posicionamento. |
| **2009-15** | **Flexbox** | (Adoção ampla em 2015). Mudança de paradigma: o foco passa a ser o alinhamento e distribuição de espaço de forma dinâmica (unidimensional: linha **ou** coluna). |
| **2014-17** | **Sticky** | Surgimento do **`position: sticky`**. Um híbrido: o elemento se comporta como `relative` até atingir um ponto da rolagem, tornando-se `fixed`. |
| **2017** | **CSS Grid** | O ápice do layout: sistema bidimensional (linhas **e** colunas simultâneas). Projetado para layouts complexos de larga escala. |




3. Parte 2 — Por que "Cascading" (Cascata)?

O termo Cascata refere-se à hierarquia de prioridade que o navegador usa para
decidir qual regra aplicar quando há conflitos.

A Analogia da Hierarquia Militar

Imagine que um elemento HTML é um soldado recebendo ordens:

1.  General (Arquivo CSS Externo): "Vista uniforme azul."
2.  Capitão (Tag <style> no HTML): "Vista uniforme verde."
3.  Sargento (Atributo style="" direto na tag): "Vista uniforme vermelho agora!"

Resultado: O soldado veste vermelho, pois a ordem dada "na cara dele" (mais
próxima/específica) vence a cascata.

4. Parte 3 — Anatomia da Sintaxe

seletor {
  propriedade: valor;
}

  - Seletor: Quem eu quero estilizar? (O alvo).
  - Propriedade: O que eu quero mudar? (Cor? Tamanho? Borda?).
  - Valor: Qual o novo ajuste? (Azul? 20px? Sólida?).

5. Parte 4 — As 3 Formas de Aplicar CSS

5.1 Inline (O Sargento)

Aplicado diretamente na tag HTML.

<p style="color: blue;">Texto azul</p>

  - Vantagem: Rápido.
  - Desvantagem: Impossível de manter em sites grandes.

5.2 Interno (O Capitão)

Escrito dentro da tag <style> no <head>.

<style>
  p { color: green; }
</style>

5.3 Externo (O General) — Padrão de Mercado

Um arquivo separado com extensão .css.

<link rel="stylesheet" href="style.css">

  - Vantagem: Um único arquivo controla a aparência de milhares de páginas.

6. Parte 5 — O Box Model (Modelo de Caixa)

Este é o conceito mais importante do CSS. Para o navegador, todo elemento é uma
caixa.

A Analogia da Caixa de Presente (A Cebola)

1.  Content (Conteúdo): O presente (texto ou imagem).
2.  Padding (Preenchimento): O plástico bolha (espaço interno entre o presente e
    a borda da caixa).
3.  Border (Borda): O papelão da caixa.
4.  Margin (Margem): O espaço entre a sua caixa e a caixa de outra pessoa na
    estante.

Animação Sugerida: Use o Inspecionar Elemento (F12) do navegador. Vá na aba
"Layout" ou "Computed" e passe o mouse sobre o diagrama do Box Model para que os
alunos vejam as cores (azul, verde, laranja) brilhando na página real.

7. Parte 6 — Seletores Básicos

| Tipo         | Sintaxe | Exemplo             | Uso                           |
| :----------- | :------ | :------------------ | :---------------------------- |
| **Elemento** | `tag`   | `p { ... }`         | Todos os parágrafos.          |
| **Classe**   | `.nome` | `.btn-azul { ... }` | Grupos de elementos (vários). |
| **ID**       | `#nome` | `#topo { ... }`     | Um único elemento exclusivo.  |

8. Atividade Prática Guiada

Objetivo: Transformar o currículo da Aula 1 (HTML) em uma página moderna.

1.  Crie um arquivo chamado style.css.
2.  No HTML, dentro do <head>, adicione o link: <link rel="stylesheet"
    href="style.css">.
3.  No CSS, aplique as seguintes mudanças:

/* 1. Mudar a fonte de toda a página */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
}

/* 2. Estilizar o título principal */
h1 {
    color: darkblue;
    text-align: center;
}

/* 3. Criar um "Card" para as seções usando Box Model */
section {
    background-color: white;
    margin: 20px;
    padding: 15px;
    border-left: 5px solid darkblue;
}

9. Exercícios

1.  Teórico: O que acontece se eu definir color: red no CSS externo e color:
    blue direto na tag HTML? Por quê?
2.  Prático: No seu currículo, crie uma classe chamada .destaque com fundo
    amarelo e negrito. Aplique-a em datas ou nomes de empresas.
3.  Visual: Desenhe o Box Model de um elemento que possui: width: 100px,
    padding: 10px e border: 5px. Qual o tamanho total que esse elemento ocupa na
    tela?
4.  Game: Complete os primeiros 10 níveis do CSS Diner para praticar seletores.

10. Distribuição do Tempo (4 horas)

| Tempo  | Atividade                                                  |
| :----- | :--------------------------------------------------------- |
| 15 min | Boas-vindas e análise de sites "retrô" vs "modernos".      |
| 45 min | História do CSS e o conceito de Cascata.                   |
| 60 min | Sintaxe, Métodos de Inserção e Seletores (Tag, Class, ID). |
| 15 min | Intervalo.                                                 |
| 45 min | **O Box Model** (Teoria e Inspecionar Elemento).           |
| 60 min | Prática: Estilizando o projeto de currículo/glossário.     |

11. Fechamento

Resumo da aula:

  - HTML = Estrutura.
  - CSS = Estética e Design.
  - Separar os dois é essencial para a manutenção.
  - O Box Model controla o espaço físico dos elementos.

Próxima aula: Layouts Flexíveis com Flexbox (Como parar de brigar com o
alinhamento das caixas).
