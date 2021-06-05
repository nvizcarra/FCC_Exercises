# Create a React Component

Otro modo de crear un comopente React, es con la *class syntax* de **ES6**.

Analizar el siguiente código:

```js
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <h1>Hi</h1>
    );
  }
}
```

La clase **Kitten** se extiende con la clase **React.Component**, la cual permite acceder a características de **React** como **local state** y **lifecycle hooks**.

Además, la clase **Kitten** posee un *constructor* definido que llama a **super()**. La función super() llama al constructor de la clase padre, en este caso **React.Component**. El constructor es un método especial utilizado durante la inicialización de objetos creados mediante la palabra clave class. Es una buena práctica llamar al constructor mediante la función super() y pasarle props a ambos. Ésto asegura que el componente se inicialice correctamente.

## Ejercicio 

```js
MyComponent is defined in the code editor using class syntax. Finish writing the render method so it returns a div element that contains an h1 with the text Hello React!.
```