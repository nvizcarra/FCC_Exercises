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

# [3. API para renderizar elementos HTML en el DOM](https://github.com/nvizcarra/FCC_Exercises/blob/8bb87555f0a6181522a11cceba96073cbcfb3610/03%20Front_End_Development_Libraries/React/04%20Render%20HTML%20Elements%20to%20the%20DOM.md)

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

# 8. [Crear un componente React con *Composition*](https://github.com/nvizcarra/FCC_Exercises/blob/ef03cb240d1388345e06c8c5cb137d169d1fdd22/03%20Front_End_Development_Libraries/React/09%20Create%20a%20Component%20with%20Composition.md)

```js
return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
)
```

```js
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        { /* Change code below this line */ }

        <ChildComponent />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```

# 9. [Utilizar React para renderizar componentes anidados](https://github.com/nvizcarra/FCC_Exercises/blob/ef03cb240d1388345e06c8c5cb137d169d1fdd22/03%20Front_End_Development_Libraries/React/10%20Use%20React%20to%20Render%20Nested%20Components.md)

```js
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};

const Fruits = () => {
  return (
    <div>
      { /* Change code below this line */ }
        <TypesOfFruit />
      { /* Change code above this line */ }
    </div>
  );
};

class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* Change code below this line */ }
            <Fruits />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```

# 10. [Compose de componentes React](https://github.com/nvizcarra/FCC_Exercises/blob/ef03cb240d1388345e06c8c5cb137d169d1fdd22/03%20Front_End_Development_Libraries/React/11%20Compose%20React%20Components.md)

```js
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};

const Fruits = () => {
  return (
    <div>
      { /* Change code below this line */ }
        <TypesOfFruit />
      { /* Change code above this line */ }
    </div>
  );
};

class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* Change code below this line */ }
            <Fruits />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```

# [11. Renderizar en el DOM un componente de clase](https://github.com/nvizcarra/FCC_Exercises/blob/ef03cb240d1388345e06c8c5cb137d169d1fdd22/03%20Front_End_Development_Libraries/React/12%20Render%20a%20Class%20Component%20to%20the%20DOM.md)

```js
// El primer arg es el componente React que quiero renderizar
// El segundo arg es el nodo del DOM en donde quiero renderizar el componente
ReactDOM.render(componentToRender, targetNode)
```
Los componentes de React pasan al React.DOM.render() de una forma diferente de los elementos JSX. Para pasar un elemento JSX, se pasa el nombre del elemento a renderizar. En cambio, para los componentes React, hay que usar la sintaxis similar al renderizado de un componente anidado, por ejemplo:

*Esta sintaxis se utiliza tanto para los componentes de clase ES6 y los functional components.*

```js
ReactDOM.render(<ComponentToRender />, targetNode)
```
