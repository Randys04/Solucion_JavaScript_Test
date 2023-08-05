
## Variables y operaciones

### 1 Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?
Una variable es un espacio en memoria reservado para almacenar información/datos.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?
Declarar una variable se refiere a únicamente darle nombre a la variable sin indicarle que dato almacenara, es como decirle al lenguaje qu creamos una varible mientras que inicializarla se refiere a darle un valor a almacenar esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
Cuando sumamos números lo que realizamos es una suma común como por ejemplo 10 + 10 = 20, y cuando concatenamos strings lo que hacemos es unir dos cadenas de texto. Ejemplo: "Hola " + “amigo” = “Hola amigo”.

- ¿Cuál operador me permite sumar o concatenar?
El operador que nos permite concatenar y sumar es +. Cunado lo usamos con numeros sumamos y cuando lo usamos con cadenas concatenamos. 

### 2 Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre
- Apellido
- Nombre de usuario en Platzi
- Edad
- Correo electrónico
- Mayor de edad
- Dinero ahorrado
- Deudas

Nombre: String; “Steven”

Apellido: String; “Moya”

Nombre de usuario Platzi: String; “stevenmoya02”

Edad: Number; 21

Correo electronico: String “stevenmoya02@gmail.com”

Mayor de edad: Boolean; True

Dinero ahorrado: Number; 100000.00

Deudas: Number; 100000.00

### 3 Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```javascript
let nombre = "Steven";
let apellido = "Moya";
let userNamePlatzi = "stevenmoya02";
let age = 21;
let email = "stevenmoya02@gmail.com";
let mayorEdad = true;
let dineroAhorrado = 100000;
let deudas = 100000;
```

### 4 Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)
```javascript
console.log(`Nombre completo: ${nombre} ${apellido}`);
console.log( `Dinero total: ${dineroAhorrado - deudas}` );
```

## Funciones

### 1 Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?
Una función es un pedazo de código, o una serie de instrucciones que realizan una operación. Una función puede retornar un valor de salida o no. Basicemnte una funcion guarda un bloque de codigo para poder ser reutilizado las veces que sea necesario.

- ¿Cuándo me sirve usar una función en mi código?
Una función es útil en nuestro código cuando repetimos mucho código, en lugar de estar repitiendo código podríamos pasarlo a una función donde solo lo tendríamos que escribir una vez y usarlo las veces que se necesite. Ademas nos sirve para separa en partes mas pequeñas bloques grandes de código, donde cada una de esas partes tenga una tarea especifica.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
Los parámetros se definen a con la función y son los datos que una función espera recibir, mientras que los argumentos son los datos que se envían a la hora de invocar a una función. Basicamente los parámetros los definimos cuando creamos la función y los argumentos se envian cuando ejecutamos la función.

### 2 Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
```javascript
const mensajeNombre = (nombre, apellido, apodo) => {
    console.log(`Mi nombre es ${nombre} ${apellido}, pero prefiero que me digas ${apodo}.`);
}

mensajeNombre("Steven", "Moya", "Randys");
```
## Condicionales

### 1 Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?
Un condicional es una porción de código que se se ejecuta de una forma u otra dependiendo de una condición o validación.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
En JavaScript existen los siguientes condicionales: if, if else, else if, switch, operador ternario. En el caso de if se ejecuta si la condición es verdadera, en el else if básicamente son if anidados, en el if else se ejecuta el if si la condición es verdadera y el else en caso de que sea falsa, el operador ternario es como un if else pero con una sintaxis mas corta. Y el switch es un bloque de código que evalua diferentes opciones.

- ¿Puedo combinar funciones y condicionales?
Sí, puede combinar funciones con condicionales

### 2 Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```
```javascript
if (tipoDeSuscripcion == "Free"){
    console.log("Solo puedes tomar los cursos gratis");

} else if (tipoDeSuscripcion == "Basic"){
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");

} else if (tipoDeSuscripcion == "Expert"){
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");

} else if (tipoDeSuscripcion == "ExpertPlus"){
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

### 3 Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏

```javascript
let suscripcion = "expertPlus";

const tiposSub = {
    free : "Solo puedes tomar los cursos gratis",
    basic : "Puedes tomar casi todos los cursos de Platzi durante un mes",
    expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
    expertPlus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año",
}


if(tiposSub[suscripcion]){
	console.log(tiposSub[suscripcion]);
} else {
	console.log("No existe este tipo de suscripcion");
}
```

## Ciclos

### 1 Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
Un ciclo es un estructura de control que nos permite ejecutar una porción de código varias veces hasta que se cumpla una condición.

- ¿Qué tipos de ciclos existen en JavaScript?
En javascript existen los siguientes ciclos: for, while, do-while.

- ¿Qué es un ciclo infinito y por qué es un problema?
Un bucle infinito es cuando la condición de un ciclo para terminar nunca se cumple por lo que el código se ejecutara infinitas veces provocando que se rompa el código y no se pueda avanzar en la ejecución.

- ¿Puedo mezclar ciclos y condicionales?
Sí, se pueden combinar bucles y condicionales.

### 2 Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```
```javascript
let i = 0;
while(i < 5){
    console.log("El valor de i es: " + i);
    i++;
}

```
```javascript
i = 10;
while(i >= 2){
    console.log("El valor de i es: " + i);
    i--;
}
```

### 3 Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```javascript
let respueta = false;

do{
    let userRespuesta = prompt("cuanto es 2 + 2")

    if(userRespuesta == 4){
        respueta = true;
        alert("Es correcto!!!");
    }else{
        alert("Incorrecto, intenta de nuevo");
    }

}while(respueta == false)
```

## Listas

### 1 Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
Un array es una estructura de datos que permite almacenar múltiples datos en una sola variable, cada dato tiene una posición única que se conoce como índice y que se usa para acceder a dichos datos. Es basicamente una lista de elementos.
Ejemplo:

```javascript
const numbers= [10, 20, 30, 40];

```
- ¿Qué es un objeto?
Un objeto es una estructura de datos que es una entidad al que se le pueden definir atributos y métodos agrupados y que pertenecen a esa entidad. Es basicamente una lista de elementos pero con la diferencia de que cada elemento tiene un nombre clave.
Ejemplo:
```javascript
const persona = {
	 nombre: "Steven",
	  edad: 22,
	  pais: "Costa Rica"
};
```
- ¿Cuándo es mejor usar objetos o arrays?
Los arrays es mejor usarlos cuando queremos crear una lista de números o cosas y poder ordenarla y acceder a su contenido a través de su posición o numero de índice. En cambio los objetos es mejor usarlos cuando queremos asignar pares de clave valor, donde cada clave esta asociada a un valor en especifico.
Tambien es bueno usar los arrays cuando lo que haremos con un elemento sera lo mismo para todos los demas elementos, mientras que los objetos es mejor usarlos cuando los nombres de cada elemento son importantes para lo que vayamos a hacer.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
Sí, podemos crear arrays de objetos y también podemos crear objetos que contengan arrays como atributos.


### 2 Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```javascript
const numbers= [10, 20, 30, 40];

function imprimirPrimerValor(array){
    console.log(array[0]);
}

imprimirPrimerValor(numbers);
```

### 3 Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```javascript
const numbers= [10, 20, 30, 40];

function imprimirValoresArray(array){
    for (let i = 0; i < array.length; i++) {
        console.log(array[i]);
    }
}

imprimirValoresArray(numbers);
```
### 4 Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```javascript
const persona = {
    nombre: "Steven",
    edad: 22,
    pais: "Costa Rica"
};

function imprimirValoresObjeto(objeto){
    for (let atributo in objeto) {
        console.log(persona[atributo])
    }
}

imprimirValoresObjeto(persona);
```

