# Render HTML Elements to the DOM

Hemos aprendido que JSX es una buena herramienta para escribir código HTML dentro de JavaScript. Con React puedo renderizar el JSX directamente al DOM HTML utilizando la API de renderizado de React, conocida como 'ReactDOM'.

ReactDOM ofrece un simple método para renderizar elementos React en el DOM.

Sintáxis:

``` ReactDOM.render(componentToRender, targetNode)

En este método, el primer argumento es el elemento React o componente que queremos renderizar.
El segundo argumento es el nodo del DOM hacia el cual queremos renderizar el componente.

ReactDOM.render() tiene que ser llamado luego de la declaración de elementos JSX, primero declarando las variables antes de utilizarlas.

```
const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);
// Change code below this line

// ReactDOM.render(JSX, challenge-node);

ReactDOM.render(JSX, document.getElementById("challenge-node"));
```