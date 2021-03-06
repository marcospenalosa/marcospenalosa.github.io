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
```javascript
for (var element of mochila.equipo){
 console.log(element);
}

for (let i = 0, i < array.length(), i++){
 console.log(array[i]);
}
```

**Condicional IF**
```javascript
for (var element of mochila.equipo){
  if(element === 'cuerda'){
   console.log('Hemos encontrado le cuerda');
  }else {
    console.log('No se ha encontrado la cuerda');
  }
}
```
**Condicional IF en una línea**
```javascript
max = value < min ? value : min;
```
**Funciones de Arrays**
```javascript
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
```javascript
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
```javascript
import{ salidas } from 'grasshopper.viaje';

function tarde(tiempo){
 return tiempo.includes('pm');
};
let pmTiempo = salidas.filter(tarde);

```
**Animaciones**
```javascript
//En la librería 3D Library tiene el método .attr()
//.attr('string', num);
//.attr(atributo a modificar, valor)

blueStripe.attr('width',50).attr('height',100);

//Con 'r' modificamos el radio
circle.attr('r',50);

//Con 'x' e 'y' modificamos la posición
circle.attr('x',50).attr('y',100);

//Con 'cx' e 'cy' modificamos la distancia con respecto a la pantalla
//cx a la izquierda de la pantalla, cy a la parte de arriba
circle.attr('cx',50).attr('cy',100);

//'click' realiza el evento que le indiquemos al hacer click sobre
// el objeto
circle.attr('click',pickRamdon(color);



//Para crear formas svg.append('String');
var rect = svg.append('rect');
var circle = svg.append('circle');

//Con el atributo transform, se pueden enviar difrentes movimientos.
//'rotate' hace girar el objeto los grados que le indiquemos en la posición x e y (grados=15 x=60 y=40)
rectangle.attr('transform','rotate(15 60 40)';

//Con el método transition creamos movimiento
function moveCircles(){
 circles.transition().attr('cx',55).transition().attr('cy',55).transition().attr('r',30)
 };
 circles.on('click',moveCircles);
 
//Seleccionar varias formas en una variable con el método selectAll
var rectangles = d3.selectAll('rect');

//Seleccionar la primera forma en una variable con el método select
var firstCircle = d3.select('circle');

//Añadir un tiempo a la transición con duration()
circle.transition().duration(5500).attr('cy',15);

//Añadir una interrupción con interrupt()
bubble.interrupt().attr('r',15).attr('cx',100);

```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NDQ0MTQzNDMsLTkxMDI1NjU4LDE3ND
gyMzkxOTQsMTE1MzgxOTM3MSwxODgxODA2MDY2LDE4NjI5NzI2
NDIsLTMyOTYwNjQ3MSwtMTgzMzQ3MTgxMSwzMTA2NDQ5NTUsNT
c2NTcxOTg5LDY2NTU1Mzg4MiwxMTEyMDk0MDcwXX0=
-->