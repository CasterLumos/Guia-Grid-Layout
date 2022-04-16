# align-items #

Alinha os itens da grade ao longo do eixo do bloco (coluna) (ao contrário dos itens justificativos que se alinham ao longo do eixo em linha (linha)). Este valor se aplica a todos os itens de grade dentro do contêiner.

Valores:

- stretch - preenche toda a altura da célula (este é o padrão)
- start - alinha os itens a serem nivelados com a borda inicial de sua célula
- end - alinha os itens a serem nivelados com a borda final de sua célula
- center - alinha os itens no centro de sua célula
- baseline - alinhar itens ao longo da linha de base do texto. Há modificadores para a linha de base - primeira linha de base e última linha de base que utilizarão a linha de base da primeira ou última linha no caso de texto de várias linhas.

~~~css
.container {
  align-items: start | end | center | stretch;
}
~~~

~~~css
.container {
  align-items: start;
}
~~~

![start](https://css-tricks.com/wp-content/uploads/2018/11/align-items-start.svg)

~~~css
.container {
  align-items: end;
}
~~~

![end](https://css-tricks.com/wp-content/uploads/2018/11/align-items-end.svg)
~~~css
.container {
  align-items: center;
}
~~~

![center](https://css-tricks.com/wp-content/uploads/2018/11/align-items-center.svg)

~~~css
.container {
  align-items: stretch;
}
~~~

![stretch](https://css-tricks.com/wp-content/uploads/2018/11/align-items-stretch.svg)

Este comportamento também pode ser definido em itens individuais do grid por meio da propriedade align-self.

Há também palavras-chave modificadoras seguras e inseguras (o uso é como align-items: safe end). A palavra-chave safe significa "tentar alinhar assim, mas não se isso significar alinhar um item de tal forma que ele se mova para uma área de transbordo inacessível", enquanto que unsafe permitirá mover o conteúdo para áreas inacessíveis ("perda de dados").
