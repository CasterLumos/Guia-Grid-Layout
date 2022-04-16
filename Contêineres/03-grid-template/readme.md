# grid-template #

Uma abreviação para grid-template-rows, grid-template-columns, e grid-template-areasem uma única declaração.

Valores:

- none - ajusta as três propriedades a seus valores iniciais
- grid-template-rows / grid-template-columns 

~~~css
.container {
  grid-template: none | <grid-template-rows> / <grid-template-columns>;
}
~~~

Também aceita uma sintaxe mais complexa mas bastante prática para especificar as três. Aqui está um exemplo:

~~~css
.container {
  grid-template:
    [row1-start] "header header header" 25px [row1-end]
    [row2-start] "footer footer footer" 25px [row2-end]
    / auto 50px auto;
}
~~~

Isto equivale a:

~~~css
.container {
  grid-template-rows: [row1-start] 25px [row1-end row2-start] 25px [row2-end];
  grid-template-columns: auto 50px auto;
  grid-template-areas: 
    "header header header" 
    "footer footer footer";
}
~~~

Como o grid-template não reinicia as propriedades implícitas da grade (grid-auto-columns, grid-auto-rows, and grid-auto-flow), que é provavelmente o que você quer fazer na maioria dos casos, é recomendado o uso da propriedade grid em vez do grid-template.

