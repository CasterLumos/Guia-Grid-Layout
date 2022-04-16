# justify-content #

Às vezes, o tamanho total do grid pode ser menor do que o tamanho do item do grid. Isto pode acontecer se todos os itens de sua grade forem dimensionados com unidades não flexíveis como px. Neste caso, você pode definir o alinhamento da grade dentro do grid-container. Esta propriedade alinha a grade ao longo do eixo em linha (ao contrário do align-content que alinha a grade ao longo do eixo do coluna).

Valores:

- start - alinha a grade a ser nivelada com a borda inicial do contêiner da grade
- end - alinha a grade para ser nivelada com a borda final do recipiente da grade
- center - alinha a grade no centro do recipiente da grade
- stretch  - redimensiona os itens da grade para permitir que a grade preencha toda a largura do recipiente da grade
- space-around  - coloca uma quantidade uniforme de espaço entre cada item da grade, com espaços de meio tamanho nas extremidades mais distantes
- space-between - coloca uma quantidade uniforme de espaço entre cada item da grade, sem espaço nas extremidades mais distantes
- space-evenly  - uniformemente - coloca uma quantidade uniforme de espaço entre cada item da grade, incluindo as extremidades distantes

~~~css
.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
~~~
 
Exemplos:

~~~css
.container {
  justify-content: start;    
}
~~~

![start](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-start.svg)

~~~css
.container {
  justify-content: end;    
}
~~~

![end ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-end.svg)

~~~css
.container {
  justify-content: center;    
}
~~~

![(center) ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-center.svg)

~~~css
.container {
  justify-content: stretch;    
}
~~~

![(stretch) ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-stretch.svg)

~~~css
.container {
  justify-content: space-around;    
}
~~~

![(space-around) ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-around.svg)

~~~css
.container {
  justify-content: space-between;    
}
~~~

![(space-between) ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-between.svg)

~~~css
.container {
  justify-content: space-evenly;    
}
~~~

![(space-evenly) ](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-evenly.svg)
