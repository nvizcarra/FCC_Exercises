# Use PropTypes to Define the Props You Expect

**Proptypes** checkea que los componentes reciban props del type correcto.

Si le digo a mi componente que va a recibir un **PropType** de tipo Array pero recibe otro tipo, la consola mostrará un warning.

Es una buena práctica asignar **propTypes** cuando sabemos el tipo de Prop que vamos a recibir.

Los **propTypes** se definen de manera similar a los **defaultProps**.

> Ejemplo de función type para un prop llamado handleClick:

```js
MyComponent.propTypes = { handleClick: PropTypes.func.isRequired }
```

PropTypes.func checkea que handleClick es una función.

isRequired indica obligatoriedad.

[Más información sobre types en este link](https://reactjs.org/docs/jsx-in-depth.html#specifying-the-react-element-type)

## Ejercicio

> Define propTypes for the Items component to require quantity as a prop and verify that it is of type number.

```js
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
};

// Change code below this line
Items.propTypes = {quantity: PropTypes.number.isRequired}
// Change code above this line

Items.defaultProps = {
  quantity: 0
};

class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <Items />
  }
};
```
