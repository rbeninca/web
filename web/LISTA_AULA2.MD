Para entrega da lista pelo moodle: um repositório git, podendo ser uma pasta dentro de um repositório ou branch , utilize um nome compreensível como  Lista CSS 1. Para cada exercício crie um arquivo na pasta.
       ✅ Atividade 0 – Jogue o CSS dinner plate.https://flukeout.github.io/
       ✅ Atividade 1 – O que é uma regra CSS? Explique o conceito de regra CSS e forneça um exemplo prático que inclua um seletor, uma propriedade e um valor.
       ✅ Atividade 2 – Crie uma página HTML com um título <h1> e vários parágrafos contendo texto "Lorem Ipsum", Em cada parágrafo, use uma fonte e cor diferentes, além de marcar palavras específicas com a tag <span>, aplicando estilos personalizados a essas palavras.
       ✅ Atividade 3 – Como podemos incluir CSS em documentos HTML?
       ✅ Atividade 4 – Seja o trecho de código HTML e CSS da figura a seguir e explique porque cada regra foi aplicada em cada item.
<!DOCTYPE html>
<head>   
   <title>Exemplo especificidade de seletores</title>
   <style>
      /*regra 1*/ li{color:red;}
      /*regra 2*/ .churras{color:green;}
      /*regra 3*/ .fruta{color:gray}
      /*regra 4*/ li+li.churras{color: black;}
      /*regra 5*/ .churras[draggable="true"]{color: magenta;}
      /*regra 6*/ #lip1,#lip2,#lip3{color:blue}
      /*regra 7*/ #lip3.fruta{color:orange}
      /*regra 8*/ ol>li.churras#lip5{color:purple}
   </style>
</head>
<body>   
   <ol>
   <!--item 1--> <li id="lip0">Abacaxi</li>
   <!--item 2--> <li           class="fruta">Melão</li>
   <!--item 3--> <li id="lip2" class="fruta">Pera</li>
   <!--item 4--> <li id="lip3" class="fruta">Uva</li>
   <!--item 5--> <li id="lip4" class="fruta">Maçã</li>
   <!--item 6--> <li           class="churras">Carne</li>
   <!--item 7--> <li           class="churras">Linguiça</li>
   <!--item 8--> <li id="lip7" class="churras" draggable="true">Pão de alho</li>
   </ol>   
</body>
</html>


✅ Atividade 6 – Display e Positions.
Reconstrua o documento HTML  abaixo, e explique porquê da exibição ser assim.
Arquivo: 6a-display-.html  6b-display-.html  e 6c-display-.html
6a-display.html
 6b-display.html
 6c-display.html
 




✅ Atividade 7 – Display e Positions.
Arquivo: 7-perfil.html
Reconstrua o documento HTML  abaixo

✅ Atividade 8– Animação de Barquinho no Mar com CSS
Arquivo: 8-barquinho.html
 Utilizando HTML e CSS puro, crie uma cena animada com ao menos um barquinho e nuvem que se movimenta, conforme ilustração abaixo

Estrutura da animação:
🛶 Um barquinho:
Utilizando uma div com imagem de fundo (background-image), aplique:
	Animação com @keyframes para simular balanço (oscilar levemente).
	Movimento horizontal (ida da esquerda para a direita, em loop infinito).
🌊 Um mar animado:
	Utilize a div.mar e adicione pseudo elementos ::before e ::after com radial-gradient ou outro método criativo.
☁️ Uma nuvem animada:
	Crie uma div que simule uma nuvem com border-radius e box-shadow para formar o desenho.
	Faça a nuvem atravessar o céu lentamente com @keyframes.
📦 Sugestões:
Use position: absolute para posicionar os elementos.
Utilize z-index para garantir que o barco fique à frente das ondas.
O fundo do céu pode ser feito com linear-gradient.

📝 Objetivos da atividade:
	Praticar animação com @keyframes.
	Trabalhar camadas (z-index) e posicionamento (position, top, left, etc).
