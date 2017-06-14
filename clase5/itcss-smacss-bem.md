## SMACSS

Organiza las reglas CSS en 5 grupos:
* Base (inicialización de estilos directamente a elementos html)
* Layout (regiones en las que se divide el area de la página)
* Modules (componentes aislados de UI)
* Theme (Tipografías y color)
* State (Cambios de estado controlados por JavaScript)
 
[Sitio web smacss](https://smacss.com/)

## ITCSS

Organiza el css en capas de menor a mayor especificidad. Estas capas son
* Settings   (variables globales)
* Tools      (helpers, mixins, funciones)
* Generic    (reset, normalize)
* Base       (estilos directos a elementos html)
* Objects    (Elementos que se repite a lo largo de la aplicacion)
* Components (Componentes de UI aislados)
* Utilities  (Ajustes específicos)

[Presentacion de Harry Roberts](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)
[CSS Wizardry](https://csswizardry.com/)
[Charla sobre ITCSS](https://www.youtube.com/watch?v=1OKZOV-iLj4)
[Herramienta para testear la especificidad](https://jonassebastianohlsson.com/specificity-graph/)

##BEM

Nomenclatura para nombrar las clases HTML para crear una estructura semántica
y escalable para los componentes

* Bloque      (comoponente aislado de UI)
* Elemento    (cada elemento del componente, se usa doble guion bajo __)
* Modificador (variantes de bloques o elementos, se usa doble guion medio --)

[Sitio web BEM](http://getbem.com)
