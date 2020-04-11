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
h1{ color:red;}

/* Sencillo - Etiqueta HTML o tipo*/
h1{ color:red;}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzMzc0NzQwNTUsMTMzMDI5NTU5MSwtOT
MxMTU1MDYxLDE1MjE1MTE5NTksLTEyNTQ0OTc3MTIsLTg0ODAy
OTA2OCw1NDkyNTE1MzksLTE2NTIxNTgxMDIsMTUyMjA3MzM1N1
19
-->