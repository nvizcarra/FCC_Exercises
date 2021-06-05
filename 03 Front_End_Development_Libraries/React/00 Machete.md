# 1. Elementos JSX

1. Simples

```js
const JSX = <H1>Hello JSX!</h1>
```


2. Complejos

```js
const JSX =  <div>
                 <h1>Hola</h1>
                 <p>Saludos</p>
                     <ul>
                         <li>Item 1</li>
                         <li>Item 2</li>
                         <li>Item 3</li>
                     </ul>
             </div>
```

# 2. Comentarios

```js
{/* */}
```

# 3. API para renderizar elementos HTML en el DOM

```js
ReactDOM.render(componentToRender, targetNode)
```

# 4. Definir clase HTML in JSX

## className
```js
const JSX = (
  <div className="myDiv">
    <h1>Add a class to this div</h1>
  </div>
);
```

# 5. Tags "Self Closing"

```js
const JSX = (
  <div>
    <h2>Welcome to React!</h2> <br />
    <p>Be sure to close all tags!</p>
    <hr />
  </div>
);
```

# 6. Componente funcional sin state

> Este componente asigna una clase HTML en JSX:
```js
const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};
```

# 7. [Crear un componente React ES6](https://github.com/nvizcarra/FCC_Exercises/blob/ef03cb240d1388345e06c8c5cb137d169d1fdd22/03%20Front_End_Development_Libraries/React/08%20Create%20a%20React%20Component.md)

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

