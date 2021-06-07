# Review Using Props with Stateless Functional Components

Un *stateless funcional component* es cualquier función que acepta props y devuelve JSX.

Por otro lado, un *stateless component* es una clase que extiende React.Component, pero no utiliza un state interno.

Finalmente, un *stateful component* es un componente de clase que mantiene su propio state interno.

Cuando hablamos de *stateful components* nos referimos simplemente a componentes React.

Un patrón común es intentar crear menos state components y más stateless functional components. Esto ayuda a contener la gestión de estados en un área específica de la aplicación. Además ésto mejora el desarrollo y mantenimiento de la app, permitiendo seguir cómo los cambios de estado afectan el funcionamiento.-

## Ejercicio

> The code editor has a CampSite component that renders a Camper component as a child. Define the Camper component and assign it default props of { name: 'CamperBot' }. Inside the Camper component, render any code that you want, but make sure to have one p element that includes only the name value that is passed in as a prop. Finally, define propTypes on the Camper component to require name to be provided as a prop and verify that it is of type string.

```js
class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <Camper/>
      </div>
    );
  }
};
// Change code below this line

const Camper = (props) => {
    return (
        <div>
            <p>{props.name}</p>
        </div>
    )
};

Camper.defaultProps = { name: 'CamperBot' }

Camper.propTypes = {name: PropTypes.string.isRequired}
```


