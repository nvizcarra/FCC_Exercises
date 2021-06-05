# Define an HTML Class in JSX

Diferencias importantes entre HTML y JSX:

* Las clases HTML cuya palabra clave es class, se tienen que nombrar className en JSX, dado que en JavaScript la palabra class está reservada.

* Por lo tanto, todas las clases HTML dentro de JSX se deben escribir en camelCase.-

* La convención de nombres para todos los atributos HTML y referencias a eventos, en JSX también se escriben con camelCase. Por ejemplo: onClick y onChange.

Ejemplo:

```
const JSX = (
  <div className="myDiv">
    <h1>Add a class to this div</h1>
  </div>
);
```
