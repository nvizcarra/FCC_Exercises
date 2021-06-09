# Bind 'this' to a Class Method

Además de setear y actualizar un state, también se pueden definir métodos para la clase componente.

Una clase de método necesita la palabra clave this para poder acceder a las propiedades en la clase (similar a state and props) dentro del scope del método.

Una forma es vincular explícitamente this en el constructor, así el this queda atado a las clases de método cuando el componente inicializa.

## Ejercicio

> The code editor has a component with a state that keeps track of the text. It also has a method which allows you to set the text to You clicked!. However, the method doesn't work because it's using the this keyword that is undefined. Fix it by explicitly binding this to the handleClick() method in the component's constructor.

> Next, add a click handler to the button element in the render method. It should trigger the handleClick() method when the button receives a click event. Remember that the method you pass to the onClick handler needs curly braces because it should be interpreted directly as JavaScript.

> Once you complete the above steps you should be able to click the button and see You clicked!.

```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      text: "Hello"
    };
    // Change code below this line
    this.handleClick = this.handleClick.bind(this);
    // Change code above this line
  }
  handleClick() {
    this.setState({
      text: "You clicked!"
    });
  }
  render() {
    return (
      <div>
        { /* Change code below this line */ }
        <button onClick={this.handleClick}>Click Me</button>
        { /* Change code above this line */ }
        <h1>{this.state.text}</h1>
      </div>
    );
  }
};
```