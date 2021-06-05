# 01 Create a JSX Simple Element

1. React es una librería de código abierto, creada y mantenida por Facebook. Es una herramienta que renderiza la Interfaz de Usuario en aplicaciones web modernas.

2. React utiliza una extensión de JavaScript llamada JSX, la cual permite escribir HTML directamente dentro de JavaScript.

## Beneficios: 
```
* Permite usar el poder programático completo de JavaScript dentro de HTML
* Ayuda a mantener el código legible
* En su mayoría, JSX es similar al HTML común que hemos aprendido
```

3. De todos modos, existen algunas diferencias clave. Por ejemplo:
* Dado que JSX es una extension sintática de JavaScript, uno puede escribir código JavaScript dentro de JSX. Para ello se tiene que añadir el código JavaScript entre llaves { 'código JavaScript' }

4. Debido a que JSX no es código JavaScript de por sí, hay que compilarlo. Para ello la herramienta más popular es Babel. 

5. It's worth noting that under the hood the challenges are calling ReactDOM.render(JSX, document.getElementById('root')). This function call is what places your JSX into React's own lightweight representation of the DOM. React then uses snapshots of its own DOM to optimize updating only specific parts of the actual DOM.

The following code uses JSX to assign a H1 element to the constant JSX:

```
const JSX = <H1>Hello JSX!</h1>
```

