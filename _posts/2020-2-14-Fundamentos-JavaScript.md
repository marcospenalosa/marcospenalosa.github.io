---
layout: post
title: Fundamentos JavaScript
categories: [JavaScript, Apuntes]
tags: [JavaScript, básicos, fundamentos]
---

### Los apuntes más básico de JavaScript:

**Variables** _(para vectores usar [ ])_
```Javascript
var mochila = {
 comida: 'platanos',
 equipo: ['mapa', 'cuerda', 'compás'],
 ropa: 'chaqueta',
};
print(mochila.comida);
print(mochila.equipo);
print(mochila.ropa);
```

**Bucle For** 
```Javascript
for (var element of mochila.equipo){
 print(element);
}
```

**Condicional IF**
```Javascript
for (var element of mochila.equipo){
  if(element === 'cuerda'){
   print('Hemos encontrado le cuerda');
  }else {
    print('No se ha encontrado la cuerda');
  }
}
```
