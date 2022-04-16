# grid-template-areas #

Define um modelo de grid referenciando os nomes das grid areas que são especificadas com a propriedade do grid. A repetição do nome de uma área da grade faz com que o conteúdo abranja essas células. Um período significa uma célula vazia. A própria sintaxe fornece uma visualização da estrutura da grade.

Valores:

- <nome da área da grade> - o nome de uma área da grade especificada com a propriedade grid-area
- . - um período significa uma célula de grade vazia
- none - não são definidas áreas de grade

~~~css
.container {
  grid-template-areas: 
    "<grid-area-name> | . | none | ..."
    "...";
}
~~~

Exemplo:

~~~css
.container {
  display: grid;
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
.item-a {
  grid-area: header;
}
.item-b {
  grid-area: main;
}
.item-c {
  grid-area: sidebar;
}
.item-d {
  grid-area: footer;
}
~~~

Isso criará uma grade que tem quatro colunas de largura por três linhas de altura. Toda a linha superior será composta pela área do cabeçalho. A linha do meio será composta de duas áreas principais, uma célula vazia e uma área da barra lateral. A última linha é toda de rodapé.

![layout](https://css-tricks.com/wp-content/uploads/2018/11/dddgrid-template-areas.svg)

Cada linha em sua declaração precisa ter o mesmo número de células.

Você pode usar qualquer número de períodos adjacentes para declarar uma única célula vazia. Desde que os períodos não tenham espaços entre eles, eles representam uma única célula.

Note que você não está nomeando linhas com esta sintaxe, apenas áreas. Quando você usa esta sintaxe, as linhas em ambas as extremidades das áreas estão sendo nomeadas automaticamente. Se o nome de sua área de grade for foo, o nome da linha da linha inicial da área e da linha da coluna inicial será foo-start, e o nome de sua última linha da linha da linha e da última linha da coluna será foo-end. Isto significa que algumas linhas podem ter vários nomes, como a linha da extrema esquerda no exemplo acima, que terá três nomes: header-start, main-start, e footer-start.