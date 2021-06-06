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

Ejemplo:

```js
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* Change code below this line */}
        <Fruits />
        <Vegetables />
        {/* Change code above this line */}
      </div>
    );
  }
};

// Change code below this line

ReactDOM.render(<TypesOfFood />, document.getElementById("challenge-node"));
```

# [12. Renderizar un class component en el DOM.](https://github.com/nvizcarra/FCC_Exercises/blob/511a414e63183dfd180c11fb53a8d62da0849b67/03%20Front_End_Development_Libraries/React/12%20Render%20a%20Class%20Component%20to%20the%20DOM.md)

```js
ReactDOM.render(<ComponentToRender />, targetNode)
```

# [13. Creando un componente React desde 0.](https://github.com/nvizcarra/FCC_Exercises/blob/f984b286e0ae0296239e43a7892f279c79ea1668/03%20Front_End_Development_Libraries/React/13%20Write%20a%20React%20Component%20from%20Scratch.md)

```js
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
    }

    render() {
        return (
        <div id='challenge-node'>
            <h1>My First React Component!</h1>
        </div>
        );
    }
};

ReactDOM.render(<MyComponent />, document.getElementById("challenge-node"));
```
# [14. Pass Props to a Stateless Functional Component](https://github.com/nvizcarra/FCC_Exercises/blob/edca8b3e7e8dc99121b88d696b67fe4a4a384f6f/03%20Front_End_Development_Libraries/React/14%20Pass%20Props%20to%20a%20Stateless%20Functional%20Component.md)

> There are Calendar and CurrentDate components in the code editor. When rendering CurrentDate from the Calendar component, pass in a property of date assigned to the current date from JavaScript's Date object. Then access this prop in the CurrentDate component, showing its value within the p tags. Note that for prop values to be evaluated as JavaScript, they must be enclosed in curly brackets, for instance date={Date()}.


```js
const CurrentDate = (props) => {
  return (
    <div>
      { /* Change code below this line */ }
      <p>The current date is: {props.date}</p>
      { /* Change code above this line */ }
    </div>
  );
};

class Calendar extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>What date is it?</h3>
        { /* Change code below this line */ }
        <CurrentDate date={Date()} />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```

# [15. Pass an Array as Props]()


