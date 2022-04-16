# grid-template-columns E  grid-template-rows #

Define as colunas e as grid lines com uma lista de valores separados por espaço. Os valores representam o tamanho da área, e o espaço entre eles representa a grid line.

~~~css
.container {
  grid-template-columns: ...  ...;
  /* e.g. 
      1fr 1fr 
      minmax(10px, 1fr) 3fr
      repeat(5, 1fr)
      50px auto 100px 1fr
  */
  grid-template-rows: ... ...;
  /* e.g. 
      min-content 1fr min-content
      100px 1fr max-content
  */
}
~~~

As grid lines são automaticamente atribuídas números positivos dessas atribuições (-1 sendo uma alternativa para a última linha).

![linhas de grade](https://css-tricks.com/wp-content/uploads/2018/11/template-columns-rows-01.svg)

Mas você pode optar por nomear explicitamente as linhas. Observe a sintaxe de conchetes para os nomes das linhas:

~~~css
.container {
  grid-template-columns: [first] 40px [line2] 50px [line3] auto [col4-start] 50px [five] 40px [end];
  grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];
}
~~~

![grid line](https://css-tricks.com/wp-content/uploads/2018/11/template-column-rows-02.svg)

Note que uma linha pode ter mais de um nome. Por exemplo, aqui a segunda linha terá dois nomes: linha1-fim e linha2-arranque:

~~~css
.container {
  grid-template-rows: [row1-start] 25% [row1-end row2-start] 25% [row2-end];
}
~~~

Se sua definição contém partes repetidas, você pode usar a notação repeat() para racionalizar as coisas:

~~~css
.container {
  grid-template-columns: repeat(3, 20px [col-start]);
}
~~~

O que é equivalente a isto:

~~~css
.container {
  grid-template-columns: 20px [col-start] 20px [col-start] 20px [col-start];
}
~~~

Se várias linhas compartilham o mesmo nome, elas podem ser referenciadas pelo nome de sua linha e contar.

~~~css
.item {
  grid-column-start: col-start 2;
}
~~~

A unidade fr permite definir o tamanho de uma área como uma fração do espaço livre do grid container. Por exemplo, isto ajustará cada item para um terço da largura do contêiner de grade:

~~~css
.container {
  grid-template-columns: 1fr 1fr 1fr;
}
~~~

O espaço livre é calculado após qualquer item não flexível. Neste exemplo, a quantidade total de espaço livre disponível para as unidades fr não inclui os 50px:

~~~css
.container {
  grid-template-columns: 1fr 50px 1fr 1fr;
}
~~~
