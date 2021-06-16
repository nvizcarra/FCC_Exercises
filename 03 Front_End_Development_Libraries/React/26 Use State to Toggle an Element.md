# Use State to Toggle an Element

Algunas veces es necesario saber el estado anterior antes de actualizar el state.

However, state updates may be asynchronous - this means React may batch multiple setState() calls into a single update. This means you can't rely on the previous value of this.state or this.props when calculating the next value. So, you should not use code like this:

De todos modos, las actualizaciones de state pueden ser asincronas lo cual significa que React puede agrupar multiples llamadas setState() en un simple update.

Esto significa que no se puede depender del valor previo de this.state o this.props cuando se calcula el siguiente valor.

Por lo tanto, evitar escribir el código de la siguiente manera:

```js
this.setState({
  counter: this.state.counter + this.props.increment
});
```

En su lugar, se debe pasar setState una función que permite acceder a state y props.

Usar una función con setState garantiza que se está trabajando con la el máximo posible de los valores actuales del state y las props.

Entonces una forma correcta de escribir correctamente sería la siguiente: 

```js
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));
```

También se puede utilizar una forma sin props si solo necesitamos el state:
```js
this.setState(state => ({
    counter: state.counter + 1
}));

NOtar que hay que envolver el objeto literal parenteses, de otro modo JavaScript pensará que es un bloque de código
```

# Ejercicio

MyComponent has a visibility property which is initialized to false. The render method returns one view if the value of visibility is true, and a different view if it is false.

Currently, there is no way of updating the visibility property in the component's state. The value should toggle back and forth between true and false. There is a click handler on the button which triggers a class method called toggleVisibility(). Pass a function to setState to define this method so that the state of visibility toggles to the opposite value when the method is called. If visibility is false, the method sets it to true, and vice versa.

Finally, click the button to see the conditional rendering of the component based on its state.

Hint: Don't forget to bind the this keyword to the method in the constructor!

```js


```
