# Explore Differences Between the var and let Keywords

En el JS clásico se podía sobrescribir declaraciones de variable accidentalmente, sin que aparezca un error.

> En este caso el resultado sería "David":
```js
var camper = 'James';
var camper = 'David';
console.log(camper);
```

Las variables **let** de ES6 resuelven este problema.

> En este caso el resultado mostraría un error en la consola del navegador:
```js
let camper = 'James';
let camper = 'David';
```

## Activar modo estricto
> El código termina de ejecutarse cuando la app presenta errores en el código o acciones "inseguras. Por ejemplo en el siguiente caso, el error mostrará que **x** no está definida:

```js
"use strict";
x = 3.14;
```

## Ejercicio
Update the code so it only uses the let keyword.

```js
let catName;
let quote;
function catTalk() {
  "use strict";

  catName = "Oliver";
  quote = catName + " says Meow!";

}
catTalk();
```
