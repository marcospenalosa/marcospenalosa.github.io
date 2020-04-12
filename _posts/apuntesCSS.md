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

/* Clase -> Atributo de un elemento HTML o XML */
/* Selectores class - clases para identificar elementos */
/* Permite varias clases separadas por un espacio */
/* <h1 class="title center">Título</h1> */
.title{
 background: yellow;
 color:red;
}
.center{
 text-align: center;
 }
/* ID -> Identificador único (se recomienda solo para JavaScript, porque no se pueden reutilizar) */
#title{
 background: yellow;
 /* * -> Selector UNIVERSAL */
 
}
```
[normalize.css](https://necolas.github.io/normalize.css/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ1NDU3MTg5OCwyMDUxMTQzMCwtODg1Mj
gxOTA1LC0xNTI2MjMzNjYsLTYxODc3NTk2MSwxMzMwMjk1NTkx
LC05MzExNTUwNjEsMTUyMTUxMTk1OSwtMTI1NDQ5NzcxMiwtOD
Q4MDI5MDY4LDU0OTI1MTUzOSwtMTY1MjE1ODEwMiwxNTIyMDcz
MzU3XX0=
-->