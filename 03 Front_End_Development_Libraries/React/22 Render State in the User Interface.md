# Render State in the User Interface

Para acceder a los valores del state dentro de un return, hay que poner el valor entre llaves.

React utiliza un DOM virtual para hacer seguimiento de los cambios detrás de escena.

Cuando el state se actualiza, se dispara nuevamente el renderizado de los componentes utilizando el nuevo dato.

Al crear un componente stateful, los demás componentes no conocen el state del primero.

El state está encapsulado o es local al componente, a menos que pasemos el dato del state a un componente hijo en un props.

## Ejercicio

> In the code editor, MyComponent is already stateful. Define an h1 tag in the component's render method which renders the value of name from the component's state.

> Note: The h1 should only render the value from state and nothing else. In JSX, any code you write with curly braces { } will be treated as JavaScript. So to access the value from state just enclose the reference in curly braces.

```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    return (
      <div>
        { /* Change code below this line */ }
        <h1>{this.state.name}</h1>
        { /* Change code above this line */ }
      </div>
    );
  }
};
```
