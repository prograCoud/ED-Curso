# OOCSS CSS Orientado a Objetos

En Diseño, Desarrollo y Marketing Digital se suele oir la frase **"El contenido es el Rey"**.

Desde la perspectiva de un desarrollador, algunos pueden argumentar que **"La velocidad es el Rey"**.

En los últimos años muchos ingenieros de front-end con experiencia han ofrecido sus sugerencias sobre cómo podemos mejorar la experiencia del usuario a través de mejores prácticas en el rendimiento.

Mientras que muchos desarrolladores (por buenas razones) se centran en gran medida en el rendimiento de JavaScript, suelen olvidarse de la optimización del CSS.

Su propósito es fomentar la reutilización de código y generar hojas de estilo más rápidas y eficientes que son más fáciles de añadir y mantener.

Se basa en dos principios fundamentales:

1. SEPARA LA ESTRUCTURA (HTML), DE LA PRESENTACIÓN (CSS)
1. SEPARA EL CONTENIDO, DE SUS CONTENEDORES

## SEPARA LA ESTRUCTURA (HTML), DE LA PRESENTACIÓN (CSS)

Casi todos los elementos de estilo de una página web tiene diferentes características visuales que se repiten en diferentes contextos. Piense en la marca de un sitio web: los colores, usos sutiles de gradientes o bordes visibles. Por otro lado, las estructuras igualmente se repiten.

Cuando estas características diferentes se abstraen en módulos basados en clases, se convierten en reutilizables y se puede aplicar a cualquier elemento y tienen el mismo resultado básico. Vamos a comparar algunos antes y después de código para que pueda ver lo que estoy hablando.

Antes de aplicar los principios OOCSS, es posible que tenga CSS que tiene este aspecto:

```css
#button {
  width: 200px;
  height: 50px;
  padding: 10px;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}

#box {
  width: 400px;
  overflow: hidden;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}

#widget {
  width: 500px;
  min-height: 200px;
  overflow: auto;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
```

Los tres elementos anteriormente tienen estilos que son únicos para cada uno, y son aplicados con el selector de ID no reutilizable para definir los estilos. Pero también tienen una serie de estilos en común. Los estilos comunes podrían existir a efectos de identificación o la coherencia del diseño.

Con un poco de planificación y previsión, podemos abstraer los estilos comunes y el CSS terminaría de esta manera:

```css
.button {
  width: 200px;
  height: 50px;
}

.box {
  width: 400px;
  overflow: hidden;
}

.widget {
  width: 500px;
  min-height: 200px;
  overflow: auto;
}

.skin {
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
```

Ahora todos los elementos están utilizando las clases, los estilos comunes se combinan en una “piel” reutilizable y nada se repite innecesariamente. Sólo tenemos que aplicar la clase a todos los elementos y el resultado será el mismo que en el primer ejemplo, excepto con menos código y una posibilidad para su posterior reutilización.

## SEPARA EL CONTENIDO, DE SUS CONTENEDORES

El segundo principio nos dice que hay que separar los contenedores de su contenido, por ejemplo:

```css
#sidebar h3 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: .8em;
  line-height: 1;
  color: #777;
  text-shadow: rgba(0, 0, 0, .3) 3px 3px 6px;
}
```

Estos estilos se aplicarán a cualquier h3 que este dentro de #sidebar. Pero si quisieramos aplicar exactamente los mismos estilos a los h3 de un #footer, con excepción de un tamaño de fuente diferente y una sombra al texto modificado, entonces tendríamos que hacer algo como esto:

```css
#sidebar h3, #footer h3 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 2em;
  line-height: 1;
  color: #777;
  text-shadow: rgba(0, 0, 0, .3) 3px 3px 6px;
}

#footer h3 {
  font-size: 1.5em;
  text-shadow: rgba(0, 0, 0, .3) 2px 2px 4px;
}
```

O podríamos terminar con algo peor:

```css
#sidebar h3 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 2em;
  line-height: 1;
  color: #777;
  text-shadow: rgba(0, 0, 0, .3) 3px 3px 6px;
}

#footer h3 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1.5em;
  line-height: 1;
  color: #777;
  text-shadow: rgba(0, 0, 0, .3) 2px 2px 4px;
}
```

Ahora innecesariamente duplicamos estilos, y puede ser que no se den cuenta (o simplemente no les importa).

OOCSS, nos anima a dar más previsión a lo que es común entre los diferentes elementos, separar esas características comunes en módulos u objetos, que pueden ser reutilizados en cualquier lugar.

Los estilos que se declaran utilizando el selector descendiente no son reutilizable , ya que son dependientes de un contenedor en particular.

Cuando usamos la construcción del módulo basado en la clase de OOCSS, nos aseguramos de que nuestros estilos no dependen de ningún elemento que contiene. Esto significa que se pueden volver a utilizarse en cualquier lugar en el documento, independientemente del contexto estructural.

```css
.subtitle-h3 {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1;
  color: #777;
}

.font-2 { font-size: 2em; }

.font-1_5 { font-size: 1.5em; }

.text-shadow-black-2-2-4 { text-shadow: rgba(0, 0, 0, .3) 2px 2px 4px; }

.text-shadow-black-3-3-6 { text-shadow: rgba(0, 0, 0, .3) 3px 3px 6px; }
```

## Beneficios de OOCSS

* Sitios Web Más Rápidos.
* Hojas de Estilos Mantenibles y Escalables.
* Evita el uso de:
  * Identificadores (sólo usalos para JavaScript)
  * Selectores descendientes
  * !important
  * Clases a las etiquetas HTML pe div.header o h1.title

Obviamente habrá ocasiones en que algunas de estas reglas será quebrada, pero en general, estos son los buenos hábitos para desarrollar y dará lugar a hojas de estilo más pequeñas y fáciles de mantener.
