---

layout: post

title: Apuntes del curso de diseño UI

categories: [cursos, tutoriales]

tags: [diseño, UI, interfaces]

---

### _Diseño de Interfaces básico_
####  [Curso de introducción al diseño de interfaces básico (en inglés)](https://scrimba.com/g/gdesign)

He visto este curso básico de diseño de interfaces donde se explica de modo ameno y en una plataforma muy interactiva unos consejos básicos a la hora de realizar cualquier tipo de diseño de interfaces.

#### Consideraciones básicas:
##### Espacios en blanco
Hay que usar correctamente las propiedades del padding, margin, line-height, etc, para dejar unos espacios mínimos entre los objetos.
##### Alineación
Tenemos que pensar que la interfaz está *dividida* en columnas y filas, así nos será más fácil buscar alinear los elementos para que tenga sensanción de uniformidad.
##### Contraste
Hay un contraste mínmo y recomendado que mantener para considerar que está correcto.
|  | Texto "pequeño" | Texto "grande" |
| :--: |  :--: | :--: |
| **Mínimo**| 4,5 : 1 | 3 : 1 |
|**Recomendado**| 7 : 1 | 4,5 : 1 |

Para saber **si** cumplimos esta condición con los diferentes colores del texto y los fondos, hay muchos plugins para navegadores web o páginas web que nos los indica, como por ejemplo: [comprueba el contraste con webaim.org](https://webaim.org/resources/contrastchecker/)
##### Escala
En esta clase utilizó una propiedad css para poder igualar todos los objetos y no dejar espacios innecesarios, dejándolo más **simétrico**.
```css
.color-container {
    grid-template-columns: repeat(3, auto);
}
```
##### Tipografía
Es recomendable no utilizar más de dos tipografías y hay que mantener correctamente la **jerarquía** de los elementos, es decir, que se vea diferente los títulos, los encabezados, textos...

##### Colores
Lo primero y más importante, no usar **muchos** colores y que no combinen correctamente.
![Correcta combinación de colores](https://raw.githubusercontent.com/marcospenalosa/marcospenalosa.github.io/master/_posts/img/apuntesDiseno/01colores.png)
### Resumen
* Espacios en blanco
* Color
* Contraste
* Escala
* Alineación
* Tipografía
* Jerarquía visual.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNTcwNDQwOTIsOTQ2NjE0MjM4LC0yMT
M3NDY0MzI4LC0yMDU1ODkyNzEyLDg3NTY1OTY2MV19
-->