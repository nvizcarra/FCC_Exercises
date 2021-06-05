# Create a Stateless Functional Component

Los componentes son el núcleo de React, ya que en eso se basa.

Una forma de crear un componente es mediante una función de JavaScript.

Hacerlo de esta manera crea un *stateless functional component*.

Un componente *stateless* puede recibir datos y renderizarlos. Pero no gestiona ni trackea cambios en los datos.

Para crear un componente con una función, hay que escribir una función JavaScript que devuelva JSX o null.

El nombre de la función si o si tiene que tener inicial mayúscula.

Ejemplo de *stateless functional component* que asigna una clase HTML en JSX:

```
const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};
```

Luego de transpilar, el <div> tendrá una clase CSS llamada customClass.

Dado que un componente JSX representa HTML, podemos juntar varios componentes para crear una web HTML compleja, lo cual es la clave de React.

Ejercicio:

The code editor has a function called MyComponent. Complete this function so it returns a single div element which contains some string of text.

Note: The text is considered a child of the div element, so you will not be able to use a self-closing tag.

```
const MyComponent = function() {
  // Change code below this line
  return (
                <div>
                  <p>texto</p>
                </div>
  );
  // Change code above this line
}
```
