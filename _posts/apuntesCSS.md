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

/* class - clases para identificar elementos */
/* Permite varias clases separadas por un espacio */
<h1 class="title center">Título</h1>
.title{
 background: yellow;
 color:red;
}
```
[normalize.css](https://necolas.github.io/normalize.css/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3MTM2OTkyMzIsLTYxODc3NTk2MSwxMz
MwMjk1NTkxLC05MzExNTUwNjEsMTUyMTUxMTk1OSwtMTI1NDQ5
NzcxMiwtODQ4MDI5MDY4LDU0OTI1MTUzOSwtMTY1MjE1ODEwMi
wxNTIyMDczMzU3XX0=
-->