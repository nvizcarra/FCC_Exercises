# Create a Stateful Component

Uno de los temas más importantes en React es el **state**.

Consiste en un dato que nuestra aplicación utiliza y que puede cambiar en el tiempo.

La idea es que la App reaccione a los cambios de **state** y actualice la UI.

Para crear un state declarando la propiedad **state** en el component class en su constructor. Se inicializa.

La propiedad **state** se tiene que setear a un objeto JavaScript.

> Ejemplo declaración state:

```js
this.state = {

}
```

Se puede acceder al state de un objeto mientras el componente perdure.

Se puede actualizar, renderizarlo, pasarlo como props a un componente hijo.

## Ejercicio
> There is a component in the code editor that is trying to render a name property from its state. However, there is no state defined. Initialize the component with state in the constructor and assign your name to a property of name.

```js
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    // Only change code below this line
    this.state = {
        name: "Name"
    }
    // Only change code above this line
  }
  render() {
    return (
      <div>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
```
