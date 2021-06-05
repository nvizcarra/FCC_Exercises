# Render a Class Component to the DOM

El código React necesita llamar a la **API ReactDOM** para renderizar en el DOM.

### Sintaxis:
```js
// El primer arg es el componente React que quiero renderizar
// El segundo arg es el nodo del DOM en donde quiero renderizar el componente
ReactDOM.render(componentToRender, targetNode)
```

Los componentes de React pasan al **React.DOM.render()** de una forma diferente de los elementos JSX. Para pasar un elemento JSX, se pasa el nombre del elemento a renderizar. En cambio, para los componentes React, hay que usar la sintaxis similar al renderizado de un componente anidado, por ejemplo:

*Esta sintaxis se utiliza tanto para los componentes de clase ES6 y los functional components.*
```js
ReactDOM.render(<ComponentToRender />, targetNode)
```

## Ejercicio:

Both the Fruits and Vegetables components are defined for you behind the scenes. Render both components as children of the TypesOfFood component, then render TypesOfFood to the DOM. There is a div with id='challenge-node' available for you to use.

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
