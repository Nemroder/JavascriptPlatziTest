# Test JavaScript - Platzi
#### Variables y operaciones
:tw-31-20e3: Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es una variable y para qué sirve?
Hace referencia al lugar en memoria en el que se guarda un objeto, el cual se identifica con un nombre especifico.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?
Declarar: Asignarle valor a la variable y nombre que la diferencia.
Inicializar: Asignarle nombre a la variable, pero no valor.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
Concatenar hace referencia a la unión de valores, a pesar de su tipo de dato. 
Al concatenar varios strings, se esta haciendo una unión de los mismos, para obtener un conjunto de cadenas de texto unificada.
En caso de concatenar un número, su resultado no sería el esperado, porque se estarían uniendo, y no sumando.

- ¿Cuál operador me permite sumar o concatenar?
Ambos se realizan con el operador de suma “+”, como lo muestra el siguiente ejemplo.
Sumar: 242 + 574
Concatenar: “Hola” + “ mundo.” + “ A esto se le llama concatenar.”

:tw-32-20e3: Determina el nombre y tipo de dato para almacenar en variables la siguiente información
- Nombre: String
- Apellido: String
- Nombre de usuario en Platzi: String
- Edad: Number
- Correo electrónico: String
- Mayor de edad: Boolean
- Dinero ahorrado: Number
- Deudas: Number

:tw-33-20e3: Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```javascript
let nombre= “Sergio”;
let apellido=“Gutierrez”;
let user= “Sergio Gutierrez”;
let edad= 19;
let correo= sergiogutierrez@gmail.com;
let mayorEdad= true;
let dineroAhorrado= 100;
let deudas= 10;
```

:tw-34-20e3: Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

```javascript
//Nombre
let nombreCompleto = nombre + " " + apellido;
console.log (`Hola mi nombre es  $("nombreCompleto")`)

//Dinero
let dineroReal = dineroAhorrado - deudas;
console.log (`Mi dinero ahorrado es  $("dinero real")`)
```
------------
#### Funciones

:tw-31-20e3: Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es una función?
Hace referencia a determinadas lineas de codigo que cumplen con tareas a realizar, que se ejecutan en base a unas condiciones.

- ¿Cuándo me sirve usar una función en mi código?
Cuando necesito llevar a cabo una tarea en especial; por ejemplo un ciclo.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
 Los parametros hace referencia a las variables y argumentos al valor de esas variables.

:tw-32-20e3: Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```javascript
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

function (completeName, nickname) {
	console.log (`Mi nombre es $ {completeName}, pero prefiero que me digas  ${nickname}.`);
}
```
------------

#### Condicionales
:tw-31-20e3: Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un condicional?
Son estructuras de control que evaluan parametros, para llevar tareas a cabo.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
Switch.
If, else, else if.
A simples rasgos ambos funcionan de forma muy similar. Switch se usa cuando tenemos bastantes opciones para tener en cuenta, dando una sensación de codigo más organizado.
Mientras que else, if y else if se puede usar tanto como sea necesario, dando la ventaja de usar alguno dentro de otro.

- ¿Puedo combinar funciones y condicionales?
Si, las funciones pueden encapsular condicionales.

:tw-32-20e3: Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```javascript
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

//My solution
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == "Free") {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion == "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion =="Expert"){
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion =="ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} else {
    console.log("No tienes suscripción")
}
```

:tw-33-20e3: Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

------------
#### Ciclos
:tw-31-20e3: Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un ciclo?
Un bucle que se repite de manera continua, hasta que la condicición especificada deje de cumplirse.

- ¿Qué tipos de ciclos existen en JavaScript?
For, while, etc.

- Qué es un ciclo infinito y por qué es un problema?
Es una bucle que se repite de manera infinita porque la condición que se usa siempre se cumple. Esto puede relentizar la pc.

- ¿Puedo mezclar ciclos y condicionales?
Si, ambos se pueden trabajar de manera alterna de ser necesario.

:tw-32-20e3: Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```javascript
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
//My solution
while (i < 5){
    let i= 0;
    i++;
    console.log("El valor de i es: " + i);
}
while (i >=1){
    let i= 10;
    i--;
    console.log("El valor de i es: " + i);
}

```
:tw-33-20e3: Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
```javascript
function suma() {
  let a = parseInt(prompt(`Escribe un numero`));
  let b = parseInt(prompt(`Escribe otro numero`));
  let operacion = parseInt(prompt(`¿Cuánto es ${a} + ${b}?`));
  let respuesta = a + b;

  if (respuesta === operacion) {
    return "Respuesta correcta";
  } else {
    return "Respuesta incorrecta";
  }
}

let resultado = suma();
console.log(resultado);
```
💡 Pista: puedes usar la función prompt de JavaScript.

------------
####Listas
:tw-31-20e3: Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un array?
Un objeto en el que se guardan otros valores.
Es una estructura de colección de datos, que se escribe dentro de [...] separado por comas.

- ¿Qué es un objeto?
Es una estructura de datos que puede contener propiedades y métodos. Se usa para representar cualquier concepto del mundo real.

- ¿Cuándo es mejor usar objetos o arrays?
Los arrays se usan para poder acceder a estos por medio de su indice. Mientras que los objetos para asignarle una propiedad a los valores.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
Si se pueden mezclar arrays con objetos y viceversa.

:tw-32-20e3:  Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```javascript
let animal= ['leon', 'perro', 'gato'];

function getArray (){
    console.log (animal[0]);
}
getArray(animal)
```
:tw-33-20e3:  Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```javascript
let estudiante = ['Juan', 'Pedro', 'Andrea'];

function getArray (estudiante){
    for (i=0; i <estudiante.length; i++){
        console.log (estudiante[i])
    }
}
getArray (estudiante);
```
:tw-34-20e3:  Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```javascript
let estudiante = {
    nombre: 'Sergio',
    apellido: 'Gutierrez',
    edad: 19
}
function getArray (Object){
    for (let key in Object){
        console.log(Object[key]);
    }
}
getArray (estudiante);
```
