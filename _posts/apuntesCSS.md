### Apuntes CSS

CSS es un lenguaje de estilos (Cascade Style Sheets) Se encarga de describir el renderizado de documentos estructurados como HTML y XML (SVG)

#### **CSS**  básico
```html
<link  rel="stylesheet"  href="sytles.css">

<!-- No recomendado, si se cargan varios y no carga uno, el resto no carga -->
<style>
 @import url('style.css');
</style>
```
[Vocabulario CSS que es cada cosa](http://apps.workflower.fi/vocabs/css/es)
#### Sintáxis usual de un documento **HTML**
```css
/*regla*/

body{ /* selector/es */ 
/* Cada línea es una declaración */
 background: red; /* Propiedad: valor*/
 margin: 10px;  
}

/* Variables en css */
:root{
 --color: red;
 }
 body{ /* selector/es */ 
/* Cada línea es una declaración */
 background: var(--color); 
}
```
#### Selectores
```css
/* Sencillo - Etiqueta HTML o tipo*/
/* Es una mala práctica, solo para normalizar */
/* Buscar normalize.css */
h1{ color:red;}

/* Sencillo - Etiqueta HTML o tipo*/
h1{ color:red;}

/* class - clases para identificar elementos*/
<h1 class="title">Título</h1>
.title{
 background: yellow;
 color:red;
}
```
[normalize.css](https://necolas.github.io/normalize.css/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc4NzMzODY5MiwtNjE4Nzc1OTYxLDEzMz
AyOTU1OTEsLTkzMTE1NTA2MSwxNTIxNTExOTU5LC0xMjU0NDk3
NzEyLC04NDgwMjkwNjgsNTQ5MjUxNTM5LC0xNjUyMTU4MTAyLD
E1MjIwNzMzNTddfQ==
-->