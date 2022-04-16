# column-gap row-gap #

Especifica o tamanho das grid lines. Você pode pensar nisso como definir a largura das margens entre as colunas/linhas.

Valores:

~~~css
.container {
  /* standard */
  column-gap: px | rem | % |  vh | vw;
  row-gap: px | rem | % |  vh | vw;
}
~~~

Exemplo:

~~~css
.container {
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  column-gap: 10px;
  row-gap: 15px;
}
~~~

![linhas de grade](https://css-tricks.com/wp-content/uploads/2018/11/dddgrid-gap.svg)

As abas são criadas apenas entre as colunas/linhas, não nas bordas externas.

## gap grid-gap ##

Uma versão curta de  column-gap row-gap

~~~css
.container {
  gap: <grid-row-gap> <grid-column-gap>;
}
~~~

Exemplo:

~~~css
.container {
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  gap: 15px 10px;
}
~~~

Se um valor de row-gap não for informado, terá o valor de column-gap
