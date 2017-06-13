# Arquitecturas CSS

* [Concepto](#arquitectura)
* [Componentes Modulares](#componentes-modulares)
* [Patrones de Diseño](#patrones-de-diseño)
* [Guías de Estilo](#guías-de-estilo)
* [Sistemas de Nomenclaturas](#sistemas-de-nomenclaturas)
* [Tipos de Arquitecturas](#tipos-de-arquitecturas)
* [Buenas Prácticas de Código](#buenas-prácticas-de-código)
* [Herramientas CSS](#herramientas-css)


## Arquitectura 

Concepto según Wikipedia: 

> 1. Arte y técnica de diseñar, proyectar y construir edificios y espacios públicos. "La arquitectura es considerada una de las bellas artes".
> 1. Técnica y estilo con los que se diseña, proyecta y construye un edificio o un monumento. "La arquitectura romana, la arquitectura gótica, la arquitectura modernista, etc".

Aplicando el concepto a CSS:

Técnicas que nos ayudan a organizar y mantener nuestro código CSS de manera óptima y saludable; abstrayéndolo y dividiéndolo en módulos y/o componentes que permitirán su reutilización y escalabilidad de manera estructurada y ordenada.

**[⬆ regresar](#arquitecturas-css)**

## Componentes Modulares 

**DIVIDE Y VENCERÁS**

> “It's a repeating visual pattern, that can be abstracted into an independent snippet of HTML, CSS and possibly JavaScript.”

> > [Nicole Sullivan](https://vimeo.com/72759139)

* Son un fragmento de la interfaz que cumple una única función.
* Son independientes, tanto de su contexto como del resto de componentes.
* Son reutilizables.
* Son autocontenidos, no filtran estilos a otros componentes.

![Componentes Modulares](http://bextlan.com/img/para-cursos/componentes-css.png)

**[⬆ regresar](#arquitecturas-css)**


## Patrones de Diseño

Los patrones de diseño son la base para la búsqueda de soluciones a problemas comunes en el desarrollo de software y otros ámbitos referentes al diseño de interacción o interfaces.

Un patrón resulta ser una solución a un problema. Para que una solución sea considerada patrón debe:

* Comprobar su efectividad resolviendo problemas similares
* Ser reutilizable, lo que significa que es aplicable a diferentes problemas en distintas circunstancias

**¿Por qué usar Patrones en CSS?**

* Construimos sistemas, no páginas
* Necesidad de modularidad
* Mejora flujo de trabajo
* Ya han sido probados y validados
* Si trabajamos en equípo mantiene el órden
* Promueven la filosofía DRY **(Don't Repeat Yourself)**

**[⬆ regresar](#arquitecturas-css)**


## Guías de Estilo

Genera un código más legible y fácil de mantener, disminuyen la cantidad de errores y refuerzan las buenas prácticas, además permiten trabajar en un mismo proyecto a varios desarrolladores

* [Airbnb CSS / Sass Styleguide](https://github.com/airbnb/css)
* [Idiomatic CSS](https://github.com/necolas/idiomatic-css)
* [CSS Guidelines](http://cssguidelin.es/)
* [Code Guide](http://codeguide.co/)
* [Primer de GitHub](http://primercss.io/guidelines/)

**[⬆ regresar](#arquitecturas-css)**


## Sistemas de Nomenclaturas

### [BEM - Bloque Elemento Modificador](https://en.bem.info/)

##### Estructura

    .bloque { ... }
    .bloque__elemento { ... }
    .bloque--modificador { ... }

##### Ejemplo

    .menu { ... }
    .menu__item { ... }
    .menu__item--active{ ... }

### [SUIT CSS - Utilidades y Componentes CSS](https://suitcss.github.io/)

##### Estructura

        .MyComponent { ... }
        .MyComponent.is-animating { ... }
        .MyComponent--modifier { ... }
        .MyComponent-part { ... }
        .MyComponent-anotherPart { ... }

##### Ejemplo

        .Menu { ... }
        .Menu.is-visible { ... }
        .Menu--active { ... }
        .Menu-item { ... }
        .Menu-link { ... }

**[⬆ regresar](#arquitecturas-css)**


## Tipos de Arquitecturas

* [OOCSS](http://oocss.org/)
* [SMACSS](https://smacss.com/)
* [7-1 Pattern​](https://sass-guidelin.es/#architecture)
* [ITCSS](http://itcss.io/)
* [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/)
* [GEL by BBC](http://www.bbc.co.uk/gel)

**[⬆ regresar](#arquitecturas-css)**


## Buenas Prácticas de Código

* Preferir **`<link>`** sobre **`@import`** para invocar hojas de estilo
* Definir siempre un **`font-size`** al elemento root (**`html`**) y hacerlo en **`px`**
* Usar [**`box-sizing: border-box;`**](http://www.paulirish.com/2012/box-sizing-border-box-ftw/)
* Estandarizar los estilos iniciales de nuestras etiquetas HTML para todos los navegadores
    * [Reset.css](http://meyerweb.com/eric/tools/css/reset/)
    * [Normalize.css](https://necolas.github.io/normalize.css/)
    * o crear uno propio :smile:
* Evitar el uso de selectores de etiquetas e identificadores y trabajar en su mayoria con clases
* Maquetar bajo un enfoque **Mobile First**
* Escribir CSS pensando en reutilizar código (**DRY**)
* Tener precaución con los shorthand de CSS
    * **`padding, margin, font, background, border, border-radius`**
    * preferible **`background-color: #FFF`** que **`background: #FFF`**
* Ordenar el código en cada selector usando la fórmula **PC-TV**:
    * Posicionamiento **`position, top, left, right, bottom, clear, z-index`**
    * Modelo de Caja **`display, float, margin, padding, width, height`**
    * Tipografía **`font-family, font-size, line-height, color, text-align`**
    * Visual **`background-color, border, border-radius, outline, opacity`**

**[⬆ regresar](#arquitecturas-css)**


## Herramientas CSS

### Frameworks

* [960 Grid System](http://960.gs/)
* [Bootstrap](http://getbootstrap.com/)
* [Foundation](http://foundation.zurb.com/)
* [Ink](http://ink.sapo.pt/)
* [Skeleton](http://getskeleton.com/)
* [Pure CSS](http://purecss.io/)
* [jQueryMobile](https://jquerymobile.com/)
* [Materialize](http://materializecss.com/)
* [MUI](https://www.muicss.com/)
* [Semantic UI](http://semantic-ui.com/)
* [Flexbox Grid](http://flexboxgrid.com/)
* [ED GRID](https://github.com/escueladigital/ed-grid)
* [Responsimple](http://jonmircha.github.io/responsimple/) :heart_eyes:
* [Comparativas entre Frameworks](http://responsive.vermilion.com/compare.php)

### Preprocesadores

![Preprocesadores](http://bextlan.com/img/para-cursos/preprocesadores.png)

Son lenguajes independientes (generalmente, más amigables, potentes y prácticos) que son capaces de traducir el código al lenguaje de destino (HTML, CSS o JavaScript), que son los únicos que los navegadores son capaces de entender de forma nativa.

El objetivo de los preprocesadores es tener un código más sencillo de mantener y editar. Incluyen características tales como variables, funciones, mixins, anidación y modularidad.

### Preprocesadores CSS

* [Less](http://lesscss.org/)
* [Stylus](http://stylus-lang.com/)
* [Myth](http://www.myth.io/)
* [Sass](http://sass-lang.com/)
    * Sintaxis Sass
    * Sintaxis SCSS

### PostCSS

Es una herramienta para transformar tu CSS con JavaScript

PostCSS es un módulo de Node.js que analiza el CSS y lo transforma en un árbol de sintaxis abstracto ([Abstract Syntax Tree](https://en.wikipedia.org/wiki/Abstract_syntax_tree))

* [PostCSS](http://postcss.org/)
* Plugins PostCSS
    * [Autoprefixer](https://github.com/postcss/autoprefixer)
    * [CSSNext](http://cssnext.io/)
    * [CSS Modules](https://github.com/css-modules/css-modules)
    * [Stylelint](http://stylelint.io/)

**[⬆ regresar](#arquitecturas-css)**