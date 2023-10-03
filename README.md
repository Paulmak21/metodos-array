# metodos-array

#[video](https://youtu.be/tCExEMROY6s)

# .forEach()

El método `.forEach()` nos permite ejecutar una función proporcionada para cada elemento de nuestra matriz. El método `.forEach()` ejecutará nuestra función de return de invocacion con 3 argumentos.

Por ejemplo:

```javascript
const array = ["Platano", "Kiwi", "Mango"];

array.forEach(fruits => console.log(fruits));

/* 
  expected output:
  "Platano"
  "Kiwi"
  "Mango"
*/
```

Debemos saber que forEach retorna `undefined`. Por eso si queremos hacer algun proceso con los datos del array debemos buscar soluciones distintas.

# .map()

El metodo `.map()` es un metodo iterativo. Invoca la funcion proporcionada una vez por cada elemento de un `array` y crea un nuevo `array` desde el resultado.

Podemos usar map para reformular objetos en un `array` :

```javascript
const nombreEdades = [
	{ nombre: 'Hans', edad: 36 },
	{ nombre: 'Paul', edad: 21 },
	{ nombre: 'Agustin', edad: 22},
];

const arregloNombreEdades = nombreEdades.map(({ nombre, edad }) => ({ [nombre]: edad}));

console.log(arregloNombreEdades); 
// [{ Hans: 36}, {Paul: 21}, {Agustin: 22}]
console.log(nombreEdades)
/* [
		{nombre: Hans, edad: 36},
		{nombre: Paul, edad: 21},
		{nombre: Agustin, edad: 22},
	] */
```

# .reduce()

El metodo `.reduce()` invoca un `callback function` en cada valor del `array` para retornar un solo valor.

En este caso vamos a usar una suma pero podriamos hacer lo mismo y restar esos valores:

```javascript
var medallas = [ 
	{ country:'US', goldMedals:39 },
	{ country:'China', goldMedals:38 }, 
	{ country:'Japan', goldMedals:27 }, 
	{ country:'UK', goldMedals:22 }, 
	{ country:'COR', goldMedals:20 }, 
	{ country:'Australia', goldMedals:17 },
	{ country:'Netherlands', goldMedals:10 },
	{ country:'France', goldMedals:10 },
	{ country:'Germany', goldMedals:10 },
	{ country:'Italy', goldMedals:10 }, ]; 
	var sum = medallas.reduce((firstVal, plusSum) => { return firstVal + plusSum.goldMedals; }, 0);

console.log(sum); // 203
```

Aqui tenemos los 10 primeros paises con mas medallas de oro en las utlimas Olimpiadas de Tokyo 2020 y si usamos esto en un console.log() deberia darnos un solo valor con la suma de todas las medallas de los respectivos paises.

# .filter()

El metodo `.filter()` crea una copia filtrada de nuestro array principal debido a los parametros dados en nuestra funcion.

Esto quiere decir que nuesto metodo `.filter()` filtrara lo que nosotros queramos de nuestro array y mostrara solo lo que le pedimos que nos muestre. Otra explicacion es utilizarla cuando queremos eliminar elementos de nuestro `array` basados en una condicion puesta por nosotros.

Por ejemplo:

```javascript
const ciudades = ['Madrid', 'Barcelona', 'Valencia', 'Alicante', 'Galicia', 'Elche',];

const filterCiudades = ciudades.filter((word) => word.length > 6);

console.log(filterCiudades);
// Expected: ['Barcelona', 'Valencia', 'Alicante', 'Galicia']
```

Tiene los mismos Parametros que `.map()`




# Diferencias entre == && ===

Doble igual (`==`) solo verifica igualdad de valores. Hace coerción de tipos inherentemente. Esto significa que antes de verificar los valores, convierte los tipos de las variables para que coincidan.

Triple igual (`===`) no hace coerción de tipos. Este verificará que las variables que estén siendo comparadas tengan el mismo valor **X** el mismo tipo de variable.

![excuseGenerator  flowChart](https://github.com/Paulmak21/metodos-array/assets/140537985/da096519-009b-4394-89e6-65faf948dd6f)

