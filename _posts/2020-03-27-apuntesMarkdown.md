---

layout: post

title: Markdown

categories: [blog, markdown]

tags: [marcado, markdown, formato]

---



### _Markdown_ para dar la forma que necesitamos al texto de forma rápida.



El principal motivo para elegir Github como zona de apuntes, es que permite el formateo del texto de forma rápida con el legunaje de marcado ***Markdown***.

Para la gente que tenga conocimientos en html, funciona de forma muy parecida, de hecho en muchas páginas web te indican las formas de conseguir los mismos resultados con ambos. Necesitamos añadir las "marcas" para que las reconozca y realizace el formato que le indicamos.

Negrita y cursiva.

```markdown
**cursiva**



**negrita**



***negrita y cursiva***
```

Viñetas

```markdown
* Viñeta 1 (hay que dejar el espacio)

* Viñeta 2

1. Lista numerada 1

2. Lista numerada 2
```

Hay **encabezados** del 1 al 6 (1 el mayor 6 el menor)

```markdown
# Encabezado 1

###### Encabezado 6
```

**Citas**:

```markdown
> Para citar texto se usa el símbolo mayor que.

"Para citar código en una línea o palabra"


​```
Para citar líneas de código 

se escribe dentro de las comillas francesas

​```

También soporta lenguajes de programación para resaltarlo
​```javascript
let i = 0;
i= i + 5;
console.log(i);
​```
```

```javascript
let i = 0;
i = i + 5;
console.log(i);
```
Para **imagenes** y **URLs**

```markdown
Para imagenes
![Texto si no carga la imagen](dirección de la imagen)

Para URL
[texto a mostrar](dirección a la que enlazar)

Imagen y URL
[![Texto a mostrar si no carga la imagen](dirección de la imagen](dirección del enlace)
```

Línea horizontal

```markdown
---
```