# align-content #

Às vezes, o tamanho total do seu grid pode ser menor do que o tamanho de seu container de grade. Isto pode acontecer se todos os itens de sua grade forem dimensionados com unidades não flexíveis como px. Neste caso, você pode definir o alinhamento da grade dentro do contêiner de grade. Esta propriedade alinha o grid ao longo do eixo da (coluna) (ao invés de justify-content que alinha a grade ao longo do eixo em linha (linha).

~~~css
.container {
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
~~~

Exemplos:

~~~css
.container {
  align-content: start;    
}
~~~

![start](https://css-tricks.com/wp-content/uploads/2018/11/align-content-start.svg)

~~~css
.container {
  align-content: end;    
}
~~~

![end ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-end.svg)

~~~css
.container {
  align-content: center;    
}
~~~

![(center) ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-center.svg)

~~~css
.container {
  align-content: stretch;    
}
~~~

![(stretch) ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-stretch.svg)

~~~css
.container {
  align-content: space-around;    
}
~~~

![(space-around) ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-around.svg)

~~~css
.container {
  align-content: space-between;    
}
~~~

![(space-between) ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-between.svg)

~~~css
.container {
  align-content: space-evenly;    
}
~~~

![(space-evenly) ](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-evenly.svg)
