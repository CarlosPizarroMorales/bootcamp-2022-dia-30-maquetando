## Que es BEM

Una metodología que nos ayuda a elegir nombre de clase semánticamente significativos. Es un acrónimo por:  

[B]loque-[E]lemento-[M]odificador.  

Se ha elegido por sobre otras metodologías de arquitectura CSS porque es muy popular, tiene una curva de aprendizaje muy corta y propuesta para los nombres de clase permite evitar conflictos en la 
cascada.

BEM utiliza la propia semántica de los elementos HTML para a partir de ellos construir los elementos principales de la metodología: los bloques. 

### Los bloques **[B]**

Deben representar sin dudas la naturaleza misma o propósito del elemento y nunca su estado. Un ejemplo es que la clase para el elemento `<header>` sería `class="header"`, pero también `navigation` para el `<nav>`, y asi con otros bloques mayores.

### Los elementos **[E]**

Si por ejemplo, el menú de nuestro website tiene una lista desordenada para sus ítems, podemos afirmar que este elemento `<ul>` no tiene sentido por si mismo fuera del bloque que lo alberga, por lo que para identificarlo adecuadamente dentro de esta metodología la podemos nombrar usando el patrón: `nombreBloque__nombreElemento` que en nuestro ejemplo de un menú dentro de un nav quedaría así:

```
<header class="header">
  <nav class="navigation">
    <ul class="navigation__list">
      <li class="navigation__item">
      ...
```

Algo importante es observar que la nomenclatura de elementos anidados debe ser `bloque__elemento` y no `bloque__elemento__elemento` por lo que por ejemplo `class="navigation__list__item"` no es correcta bajo esta metología. 

### Modificador **[M]**

Con este valor ya podemos describir apariencia, estado o comportamiento del bloque o bloque__elemento. La convención sintáctica es utilizar -- en vez de __ por ejemplo:

```
<!-- sintaxis para bloques -->
<footer class="footer footer--dark-theme">
  <small class="footer__copyright">
```

```
<!-- sintaxis para elementos -->
<form class="form">
  <div class="form__container">
    <input type="text" class="form__input form__input--focused">
```

### REFERENCIAS y lecturas: 

* [en.bem.info](https://en.bem.info/methodology/)
* [getbem.com](http://getbem.com/introduction/)
* [CSS-Tricks](https://css-tricks.com/bem-101/)
* [CSS-Tricks...again](https://css-tricks.com/building-a-scalable-css-architecture-with-bem-and-utility-classes/)

