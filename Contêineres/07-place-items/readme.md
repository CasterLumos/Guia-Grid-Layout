
# place-items #

Os place-items estabelecem tanto as propriedades de align-items quanto as propriedades de justify-items em uma única declaração.

Valores:
    O primeiro valor define o align-items, o segundo valor justify-items. Se o segundo valor for omitido, o primeiro valor é atribuído às duas propriedades.

Isto pode ser muito útil para uma centralização multidirecional super rápida:

~~~css
.center {
  display: grid;
  place-items: center;
}
~~~
