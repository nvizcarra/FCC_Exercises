# Pass Props to a Stateless Functional Component

En React se puede pasar props (propiedades) a los componentes hijos.

Si tenemos un componente App que renderiza un componente hijo llamado Welcome (stateless functional component), le podemos pasar a welcome la propiedad *user*. Por ejemplo:

```js
<App>
  <Welcome user='Mark' />
</App>
```

Dado que Welcome es un stateless functional component, tiene acceso a este valor así:

```js
const Welcome = (props) => <h1>Hello, {props.user}!</h1>
```

Se nombra props de manera estándar.

Cuando se trata de stateless functional components, el props se considera un argumento de una función que retorna JSX.

Se puede acceder al valor del argumento en el cuerpo de la función.

En un class component, se ve un poco distinto.

## Ejercicio:

> There are Calendar and CurrentDate components in the code editor. When rendering CurrentDate from the Calendar component, pass in a property of date assigned to the current date from JavaScript's Date object. Then access this prop in the CurrentDate component, showing its value within the p tags. Note that for prop values to be evaluated as JavaScript, they must be enclosed in curly brackets, for instance date={Date()}.

(Cómo pasar información de props de un componente padre a hijo)

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

[Hints](https://www.freecodecamp.org/learn/front-end-libraries/react/pass-props-to-a-stateless-functional-component)