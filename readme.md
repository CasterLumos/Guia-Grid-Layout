# Um guia completo da Grid #

CSS Grid Layout (também conhecido como "Grid" ou "CSS Grid"), é um sistema de layout bidimensional baseado em grid que, comparado a qualquer sistema de layout web do passado, muda completamente a maneira como projetamos interfaces de usuário.

O CSS sempre foi usado para layout de nossas páginas da web, mas nunca fez um bom trabalho com ele. Primeiro, usamos tabelas, depois floats, positioning e inline-block, mas todos esses métodos eram essencialmente hacks e deixavam de fora muitas funcionalidades importantes (centralização vertical, por exemplo).

O Flexbox também é uma ótima ferramenta de layout, mas seu fluxo unidirecional tem diferentes casos de uso - e na verdade eles funcionam muito bem em conjunto! Grid é o primeiro módulo CSS criado especificamente para resolver os problemas de layout que todos nós temos invadido há tanto tempo quanto temos feito websites.

## Basics & Browser Support ##

A partir de março de 2017, a maioria dos navegadores enviava suporte nativo e não fixo para o CSS Grid: Chrome (inclusive no Android), Firefox, Safari (inclusive no iOS), e Opera. O Internet Explorer 10 e 11, por outro lado, o suportam, mas é uma implementação antiga com uma sintaxe ultrapassada. A hora de construir com grade é agora!

Para começar, é preciso:

- Definir um elemento de contêiner como grid

    ~~~css
    .containerPai {
        display: grid;
    }
    ~~~

- Definir o tamanho da coluna e da linha

    ~~~css
    .containerPai {
        display: grid;
        grid-template-columns: ;
        grid-template-rows:;
    }
    ~~~

- Colocar seus elementos filhos no grid com grid-column e grid-row. 

    ~~~css
    .elementofilho {
        grid-column: ;
        grid-row: ;
    }
    ~~~

Da mesma forma que o flexbox, a ordem de fornecimento dos elementos do grid não importa. O CSS pode colocá-los em qualquer ordem, o que torna super fácil rearranjar sua grade com consultas de mídia.

Imagine definir o layout de sua página inteira, e depois reorganizá-la completamente para acomodar uma largura de tela diferente, tudo com apenas algumas linhas de CSS. O grid é um dos módulos CSS mais poderosos já introduzidos.

## Nomenclaturas ##

Antes de mergulhar nos conceitos de Grid, é importante entender a terminologia. Uma vez que os termos envolvidos aqui são todos um pouco semelhantes conceitualmente, é fácil confundi-los uns com os outros se você não memorizar primeiro seus significados definidos pela especificação do Grid. Mas não se preocupe, não há muitos deles.

### Grid Container ###

O elemento sobre o qual display: grid é aplicado. É o pai direto de todos os itens grid. Neste exemplo, a classe container é um grid container.

~~~html
<div class="container">
    <div class="item item-1"> </div>
    <div class="item item-2"> </div>
    <div class="item item-3"> </div>
</div>
~~~

### Grid Item ###

Os filhos (ou seja, descendentes diretos) do Grid Container. Aqui os elementos do item são itens do grid, mas o subitem não é.

~~~html
<div class="container">
    <div class="item"> </div>
    <div class="item">
        <p class="sub-item"> </p>
    </div>
    <div class="item"> </div>
</div>
~~~

### Grid Line ###

As linhas divisórias que compõem a estrutura do grid. Elas podem ser verticais ("linhas da coluna") ou horizontais ("linhas da linha") e residem em qualquer lado de uma linha ou coluna. Aqui a linha amarela é um exemplo de uma linha de grade de coluna.
![Grid Line](https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-line.svg)

### Grid Cell ###

É o espaço entre duas linhas de grade de colunas e duas linhas de grade de colunas, ambas adjacentes. É uma única "unidade" do grid. Aqui está a Grid Cell entre as Grid Line de linha 1 e 2, e as Grid Line de coluna 2 e 3.

![Grid Cell](https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-cell.svg)

### Grid Track ###

É o espaço entre duas linhas de grade adjacentes. Você pode pensar nelas como as colunas ou linhas da grade. Aqui está a Grid Track entre a segunda e a terceira grid lines.

![Grid Track](https://css-tricks.com/wp-content/uploads/2021/08/terms-grid-track.svg)

### Grid Area ###

É o espaço total cercado por quatro grid Lines. Uma Grid Area pode ser composta de qualquer número de Grid Cell. Aqui está a Grid Area entre as grid Lines de linha 1 e 3, e as grid Lines de coluna 1 e 3.

![Grid Area](https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-area.svg)
