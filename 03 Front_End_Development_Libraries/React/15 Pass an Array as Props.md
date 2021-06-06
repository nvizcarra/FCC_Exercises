# Pass an Array as Props

¿Cómo pasar arrays como props?

Para pasar un array a elementos JSX, tiene que ser tratado como JavaScript y envuelto entre llaves:

```js
<ParentComponent>
  <ChildComponent colors={["green", "blue", "red"]} />
</ParentComponent>
```

El siguiente código junta todos los colores del array en un string separado por comas:

```js
const ChildComponent = (props) => <p>{props.colors.join(', ')}
```

> Resultado
```js
<p>green, blue, red</p>
```

## Ejercicio:

> There are List and ToDo components in the code editor. When rendering each List from the ToDo component, pass in a tasks property assigned to an array of to-do tasks, for example ["walk dog", "workout"]. Then access this tasks array in the List component, showing its value within the p element. Use join(", ") to display the props.tasksarray in the p element as a comma separated list. Today's list should have at least 2 tasks and tomorrow's should have at least 3 tasks.


```js
const List = (props) => {
  { /* Change code below this line */ }  
  return <p>{props.tasks.join(', ')}</p>
  { /* Change code above this line */ }
};


class ToDo extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>To Do Lists</h1>
        <h2>Today</h2>
        { /* Change code below this line */ }
        <List tasks={["walk dog", "workout"]} />
        <h2>Tomorrow</h2>
        <List tasks={["walk dog", "workout", "sleep"]} />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```

[Hint](https://forum.freecodecamp.org/t/freecodecamp-challenge-guide-pass-an-array-as-props/301401)