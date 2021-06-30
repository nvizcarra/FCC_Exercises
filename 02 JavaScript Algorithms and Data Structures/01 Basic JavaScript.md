# Global Scope and Functions

El scope hace referencia a la visibilidad de las variables dentro de las distintas partes del código. Por ejemplo las variables que están definidas fuera de una función, poseen scope global y se pueden leer desde cualquier lado del código JavaScript.

# Local Scope and Functions

Las variables creadas dentro de una función, como así también los parámetros de la función, poseen scope local. Ésto significa que solo son visibles dentro de dicha función.

# Find the Length of a String

```js
console.log("Alan Peter".length);
```

# Use Bracket Notation to Find the First Character in a String

```js
var firstName = "Charles";
var firstLetter = firstName[0];
```

# Understand String Immutability

No se puede modificar caracteres individuales de un string:
```js
var myStr = "Bob";
myStr[0] = "J";
```

Si se puede modificar la variable entera del string
```js
var myStr = "Bob";
myStr = "Job";
```

# Store Multiple Values in one Variable using JavaScript Arrays

```js
var sandwich = ["peanut butter", "jelly", "bread"]
```

# Nest one Array within Another Array

```js
var myArray = [["Bulls", 23], ["White Sox", 45]];
```

# Access Array Data with Indexes

```js
var array = [50,60,70];
array[0]; // es 50
var data = array[1]; // data contiene 60
```

# Modify Array Data With Indexes

A diferencia de los strings, las entradas de los arrays se pueden modificar libremente

```js
var ourArray = [50,40,30];
ourArray[0] = 15; // [15,40,30]
```

# Access Multi-Dimensional Arrays With Indexes

Un array multi dimensional es un array de arrays

```js
var arr = [
  [1,2,3],
  [4,5,6],
  [7,8,9],
  [[10,11,12], 13, 14]
];
arr[3]; // [[10, 11, 12], 13, 14]
arr[3][0]; // [10, 11, 12]
arr[3][0][1]; // 11
```

# Manipulate Arrays With push()

push () añade datos al final de un array

```js
var arr1 = [1,2,3];
arr1.push(4); // arr1 === [1,2,3]

var arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]); // arr2 === ["Stimpson", "J", "cat", ["happy", "joy"]]
```

# Manipulate Arrays With pop()

pop() retira el último elemento de un array.

El elemento retirado se puede guardar en otra variable si se quiere.

```js
var threeArr = [1, 4, 6];
var oneDown = threeArr.pop(); 
console.log(oneDown); // oneDown === 6
console.log(threeArr); // threeArr === [1, 4]
```

# Manipulate Arrays With shift()

shift() retira el primer elemento de un array.
```js
var ourArray = ["Stimpson", "J", ["cat"]];
var removedFromOurArray = ourArray.shift(); // removedFromOurArray === Stimpson 
// ourArray ===  ["J", ["cat"]]
```

# Manipulate Arrays With unshift()

.unshift() funciona como push() pero en lugar de añadir el elemento al final del array, unshift() lo añade al inicio

```js
var ourArray = ["Stimpson", "J", "cat"];
ourArray.shift(); // ["J", "cat"];
ourArray.unshift("Happy"); // ["Happy", "J", "cat"];
```

# Write Reusable JavaScript with Functions

Las funciones son partes de código reutilizable

```js
js
function functionName() {
  console.log("Hello World");
}
```

Para invocar a la función que hemos creado se utiliza la siguiente sintaxis 

```js
functionName();
```


# Understanding Undefined Value returned from a Function

Las funciones que no poseen **return** procesan el código dentro de la función pero el valor que retornan es **undefined**.

# Assignment with a Returned Value

Una variable se puede llenar con el resultado que retorna una función:

```js
ourSum = sum(5, 12);
```


