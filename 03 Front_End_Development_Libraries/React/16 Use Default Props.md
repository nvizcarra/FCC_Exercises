# Use Default Props

También hay una opción para setear props por default para un componente.

```js
MyComponent.defaultProps = { location: 'San Francisco' }
```

## Ejercicio
> The code editor shows a ShoppingCart component. Define default props on this component which specify a prop items with a value of 0.

```js
const ShoppingCart = (props) => {
  return (
    <div>
      <h1>Shopping Cart Component</h1>
    </div>
  )
};
// Change code below this line

ShoppingCart.defaultProps = { items: 0}
```

