# Set State with this.setState

Otra forma de cambiar el state de un componente es utilizando setState.

Se llama al método setState de la siguiente manera:

```js
this.setState();
```

Al método de arriba se le pasa valor inicial y valor para actualización.

Por ejemplo:

```js
this.setState({
  username: 'Lewis'
});
```

React espera que nunca se modifique el state directamente, siempre hay que usar this.setState().

Las actualizaciones con setState pueden ser asincronas.


[Sintaxis alternativa para setState](https://facebook.github.io/react/docs/state-and-lifecycle.html)

## Ejercicio
> There is a button element in the code editor which has an onClick() handler. This handler is triggered when the button receives a click event in the browser, and runs the handleClick method defined on MyComponent. Within the handleClick method, update the component state using this.setState(). Set the name property in state to equal the string React Rocks!.

> Click the button and watch the rendered state update. Don't worry if you don't fully understand how the click handler code works at this point. It's covered in upcoming challenges.

```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'Initial State'
    };
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    // Change code below this line

    // Change code above this line
  }
  render() {
    return (
      <div>
        <button onClick={this.handleClick}>Click Me</button>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
```
