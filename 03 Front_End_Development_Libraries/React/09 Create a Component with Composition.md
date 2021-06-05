# Create a Component with Composition
Caso: Composición de una app con 3 componentes:
* Navbar
* Dashboard
* Footer

Para combinarlos, puedo crear un componente padre llamado App que será el principal y se encargará de renderizar cada uno de los 3 componentes como hijos.
Para renderizar un componente como hijo, el nombre del componente tiene que ir escrito como un tag HTML en JSX. Por ejemplo:

```js
return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
)
```

Cuando React encuentra un custom HTML tag que hace referencia a otro componente, lo renderiza en la ubicación del tag.

## Ejercicio
In the code editor, there is a simple functional component called ChildComponent and a class component called ParentComponent. Compose the two together by rendering the ChildComponent within the ParentComponent. Make sure to close the ChildComponent tag with a forward slash.

Note: ChildComponent is defined with an ES6 arrow function because this is a very common practice when using React. However, know that this is just a function. If you aren't familiar with the arrow function syntax, please refer to the JavaScript section.

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