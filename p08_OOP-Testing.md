# Práctica 8. Programación Orientada a Objetos en JavaScript. Unit Testing
### Factor de ponderación: 7

### Objetivos
Los objetivos de esta práctica son:
 
* Poner en práctica metodologías y conceptos de Programación Orientada a Objetos en JavaScript.
* Practicar el diseño y desarrollo de pruebas de software (testing) utilizando Mocha y Chai.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:

* El comportamiento del programa debe ajustarse a lo solicitado en este enunciado.
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema.
* Capacidad del programador(a) de introducir cambios en el programa desarrollado.
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la Guía de Estilo.
* El código ha de estar documentado con [JSDoc](https://jsdoc.app/). 
  Haga que la documentación del programa generada con JSDoc esté disponible a través de una web alojada en su máquina IaaS de la asignatura.
* El alumnado ha de acreditar su capacidad para configurar y ejecutar ESLint en sus programas.
* El alumnado ha de acreditar que sabe depurar sus programas usando Visual Studio Code.
* Se comprobarán los tests unitarios que el alumnado ha desarrollado para todos sus códigos usando Mocha y Chai.
* El alumnado ha de acreditar su capacidad para ejecutar los tests unitarios desde la interfaz de Visual
  Studio Code.

### Indicaciones de caracter general
Configure un fichero `package.json` diferente para cada uno de sus "proyectos" (ejercicios)
de modo que ejecutando `npm install` queden instaladas todas las dependencias del proyecto.

Algunos de los programas correspondientes a los ejercicios 1-5 de esta práctica ya han sido realizados en
sesiones de prácticas anteriores, de modo que los tests unitarios que se propone desarrollar serían 
desarrollados *a posteriori*. 
Esta no es la práctica habitual al seguir la metodología TDD sino que los tests (al igual que la
documentación) han de comenzar a desarrollarse **antes** de desarrollar el código.
Ello no es óbice para que tanto los tests como la documentación se revisen convenientemente conforme se
refactoriza el código.
Si no hubiera realizado Ud. anteriormente cualquiera de esos ejercicios, desarrolle sus correspondientes
tests usando Mocha y Chai antes de proceder a desarrollar los programas.

En cualquier caso diseñe e implemente sus propios tests en Mocha y Chai y verifique que sus programas pasan
estos tests **antes** de revisar los tests (usando Jest) que Exercism proporciona.

Independientemente de cómo se implemente una función, el desarrollador conoce de antemano los resultados que
esa función debe entregar como correctos.
Recuerde asimismo que los tests de código son en sí mismo programas y como tales han de estar correctamente
documentados.
El *hook* *describe* es posiblemente la mejor herramienta para la documentación de sus tests, pero no ha de
ser la única.
Incluya comentarios de cabecera también en los ficheros `*.spec.js` de pruebas de código.

### 1.- Tests uniarios para *Armstrong Numbers*
Cree un nuevo proyecto tomando como punto de partida el programa `armstrong-numbers.js` que resuelve el problema
[*Armstrong Numbers*](https://exercism.io/my/solutions/5e1f0bde06fb41e78acbfb2312181821)
del *track* de JavaScript de 
[Exercism](https://exercism.io/my/tracks/javascript).
Configure su proyecto para realizar tests usando Mocha y Chai.
A continuación diseñe y desarrolle tests unitarios para acreditar la corrección del programa
`armstrong-numbers.js`.
Se propone que diseñe sus tests sin revisar los tests que Exercism suministra para este ejercicio.
Compruebe que el programa pasa todos los tests que desarrolle.
Compare finalmente los tests que Ud. ha desarrollado con los que la plataforma Exercism propone para ese mismo
problema.

### 2.- Tests uniarios para *Nth Prime*
Repita el ejercicio anterior, pero en este caso para el programa `nth-prime.js` correspondiente al problema
[*Nth Prime*](https://exercism.io/my/solutions/07630f17544c4c4ca7cc30fa69c51e7e)
de Exercism.

### 1.- Tests uniarios para *Yacht*
Repita el ejercicio 1 para el programa `yacht.js` correspondiente al problema
[*Yacht*](https://exercism.io/my/solutions/5f2e1e4332fd419abf2ea365b05b4e3b)
de Exercism.

### 4.- Tests uniarios para *Darts*
Repita el ejercicio 1 para el programa `darts.js` correspondiente al problema
[*Darts*](https://exercism.io/my/solutions/de65d30c065c435b82911b0c7ca10b0c)
de Exercism.

### 5.- Tests uniarios para *Roman Numerals*
Repita el ejercicio 1 para el programa `roman-numerals.js` correspondiente al problema
[*Roman Numerals*](https://exercism.io/my/solutions/5bd5622efab448d9b12233e779696a41)
de Exercism.

### 6.- La clase *Clock*
En este ejercicio se propone desarrollar un módulo ES6 que implemente una clase `Clock` 
para representar un reloj digital con horas y minutos. No es necesario contemplar segundos.

La clase no ha de usar en modo alguno objetos 
[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
de JavaScript y se desarrollará usando la sintaxis para clases de JavaScript y poniendo en práctica los principios de
abstracción y encapsulamiento característicos de la Programación Orientada a Objetos.

La clase ha de contener un método *toString()* que permita imprimir en pantalla un objeto *Clock* en el
formato `hh:mm`.
La clase ha de contemplar métodos que permitan sumar y restar minutos a un objeto *Clock*.
Análogamente, dos objetos que representen la misma hora deben ser iguales entre sí.
Incluya discrecionalmente cualesquiera otras operaciones que considere adecuadas como métodos en la clase `Complejo`.

Previo a la implementación de la clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos de la clase.

Encapsule la clase en un módulo que exporte la misma hacia otros programas clientes que pudieran utilizarla.

Desarrolle un programa *cliente* que utilice la clase *Clock* e instancie objetos de esa clase:
```javascript
const horaActual = new Clock(11, 59);
console.log(horaActual.toString());   // 11:59h
```

### 7.- La clase *MySet*
En este ejercicio se propone desarrollar un módulo ES6 que implemente una clase `MySet` 
para representar 
[conjuntos](https://en.wikipedia.org/wiki/Set_(mathematics)) 
de números naturales.

Obviamente, si en alguna ocasión se precisa utilizar conjuntos, lo que ha de hacerse es utilizar la clase 
[Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
de JavaScript.
No obstante en este ejercicio práctico la implementación de la clase `MySet` no ha de usar en modo alguno objetos 
[Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
de JavaScript y se desarrollará usando la sintaxis para clases de JavaScript y poniendo en práctica los principios de
abstracción y encapsulamiento característicos de la Programación Orientada a Objetos.

La clase ha de contener al menos métodos (y/o atributos) que implementen las siguientes operaciones con conjuntos:
* `toString` Devuelve una cadena que representa el conjunto. Los conjuntos se imprimirán en pantalla con sus
  elementos incluídos entre llaves, de modo que el conjunto vacío se representa por `{}`.
* `size` Devuelve el cardinal del conjunto
* `union` Unión de conjuntos
* `intersection` Intersección de conjuntos
* `difference` Complemento relativo
* `contains` Determina si un elemento pertenece al conjunto
* `empty` Determina sin un conjunto es vacío
* `subset` Determina si un conjunto es subconjunto de otro 
* `disjorint` Indica si dos conjuntos son disjuntos
* `eql` Indica si dos conjuntos son iguales 
* `add` Añade un elemento a un conjunto

Para la definición de estas operaciones consulte 
[Wikipedia](https://en.wikipedia.org/wiki/Set_(mathematics)) 
así como los métodos y ejemplos de la clase
[Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) 
de JavaScript.

Incluya discrecionalmente cualesquiera otras operaciones que considere adecuadas como métodos en la clase
`MySet`.

Previo a la implementación de la clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos de la clase.

Desarrolle un programa cliente `sets.js` que permita operar con conjuntos y haga uso de la clase `MySet` que diseñe.
El programa cliente realizará operaciones similares a las que figuran en la página MDN correspondiente a la
clase
[Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) 
de JavaScript, por ejemplo:
```javascript
const mySet1 = new MySet()

mySet1.add(1)           // Set {1}
mySet1.add(5)           // Set {1, 5}
mySet1.add(5)           // Set {1, 5}
mySet1.has(Math.sqrt(25))  // true

const mySet2 = new MySet([1, 2, 3, 4])
mySet2.size                    // 4
```

Observe que el constructor de la clase toma como parámetro un array en el que figuran los elementos con los
que se inicializa el conjunto.

Por simplicidad asumiremos que los números que intervienen en los conjutos son todos mayores o iguales que 1.

Para representar internamente los conjuntos se pueden utilizar diversas ideas y se propone aquí una que podría
usarse, si lo estiman conveniente, y que se expone a continuación:

Para representar un conjunto de números (enteros positivos) se utilizarán los bits de un número. 
Si el bit i-ésimo está a 1 ello indicará que el número *i* pertenece al conjunto. 
Si ese bit está a 0, ello indica que el número *i* no pertenece al conjunto. 
De este modo se puede representar conjuntos con tantos números naturales como bits tiene la representación
binaria del número.

[JavaScript representa todos los
números](https://stackoverflow.com/questions/2802957/number-of-bits-in-javascript-numbers#:~:text=All%20numbers%20in%20JavaScript%20are,%2D%2D%20will%20be%20represented%20accurately.)
en formato de punto flotante IEEE-754, pero las operaciones de bits
las calcula sobre 32 bits (4 bytes) de modo que con un número se pueden representar conjuntos de 32
elementos (`{1, 2, 3, ..., 32}`).

Una primera aproximación sería usar este esquema limitando los conjuntos a un máximo de 32 elementos.
Si se requieren conjuntos con un mayor número de elementos sería necesario usar un vector de números.
Con un vector de `M` valores numéricos se pueden representar conjuntos con un máximo de `32 * M` elementos. 
Usando este esquema de representación resulta fácil implementar las diferentes operaciones sobre conjuntos
usando 
[aritmética de bits](https://medium.com/@soni.dumitru/javascript-bitwise-operations-190001bf1fc).
