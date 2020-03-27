---
layout: post
title: Fundamentos JavaScript
categories: [JavaScript, Apuntes]
tags: [JavaScript, básicos, fundamentos]
---

### Los apuntes más básicos de JavaScript:

Estoy aprendiendo **JavaScript** con la aplicación _Grasshopper_, así que utilizaré este post para ir apuntando lo básico que vaya apareciendo.

**Variables** _(para vectores usar [ ])_
```javascript
var mochila = {
 comida: 'platanos',
 equipo: ['mapa', 'cuerda', 'compás'],
 ropa: 'chaqueta',
};
console.log(mochila.comida);
console.log(mochila.equipo);
console.log(mochila.ropa);

//let crea la variable en modo local
let ciudad
```

**Bucle For** 
```Javascript
for (var element of mochila.equipo){
 console.log(element);
}
```

**Condicional IF**
```Javascript
for (var element of mochila.equipo){
  if(element === 'cuerda'){
   console.log('Hemos encontrado le cuerda');
  }else {
    console.log('No se ha encontrado la cuerda');
  }
}
```
**Condicional IF en una línea**
```Javascript
max = value < min ? value : min;
```
**Funciones de Arrays**
```JavaScript
// .slice(posIni, posFin) Crear un vector seleccionando las posiciones de otro. 
console.log(ciudad.slice(3,6);

// .pop() Quitar información en la posición final del vector y permite guardarla en una variable.
viajeAtlanta = viajeCiudades.pop();

// .push() Añadir información en la posición final del vector.
viajarCiudades.push(barcoAtlanta);

//.forEach() recorre cada posición del vector.
precioVuelos.forEach(compararMinimo);

```
**Funciones**
```JavaScript
//.filter() Devuelve un vector con todos los elementos que cumplan el filtro.
//Ejemplo de developer.mozilla.org

function esSuficientementeGrande(elemento) {
  return elemento >= 10;
}
var filtrados = [12, 5, 8, 130, 44].filter(esSuficientementeGrande);
// filtrados es [12, 130, 44]

//.includes() Devuelve verdadero o falso si la variable, array o matriz contiene el elemento enviado.
tiempo.includes('pm');

[1, 2, 3].includes(2);     // true
[1, 2, 3].includes(4);     // false
[1, 2, 3].includes(3, 3);  // false
[1, 2, 3].includes(3, -1); // true
[1, 2, NaN].includes(NaN); // true

```
**Importar y Crear Funciones**
```JavaScript
import{ salidas } from 'grasshopper.viaje';

function tarde(tiempo){
 return tiempo.includes('pm');
};
let pmTiempo = salidas.filter(tarde);

```

