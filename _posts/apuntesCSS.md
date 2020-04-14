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
/* <h1 id="title center">Título</h1> */
#title{
 background: yellow;
 }
 
 /* * -> Selector UNIVERSAL, no se recomienda */
 *{
 color: red; /* Todo se pone rojo */
}

/* Agrupados -> se aplica el mismo estilo a todos */
/* Separados por comas , */
/* Se recomienda una línea por selector para la lectura */
.title, 
.parrafo{
 color: red
 }

/* Descendiente -> se aplica a los hijos */
/* Separados por espacios */
/* No se recomienda su uso, al usar clases ya puedes especificar los hijos con la clase */
.list .list-item{
 color: red
 }
 
/* Seleccionar hijo directo  > */
/* La lista hija de un item de una lista, no se muestra */
/* Al pasar el ratón la muestro */
li > ul {
 diplay: none;
}
li:hover ul{
 display: block;
}

/* Seleccionar hermano siguiente + */
/* Selecciona al elemento justo depués de otro */
/* Si el elemento que sigue despues de un h1 es un p este tendrá un color rojo */  
h1 + p {  
    color:red;
}

/* Seleccionar hermanos siguienteS ~ */
/* Selecciona todos los descendientes */
/* Cualquier elemento p que esté despues de un h1 tendrá un color rojo */  
h1 ~ p {  
    color:red;
}

/* Seleccionar por atributos  [] */
/* [attr="value"] o [attr] */
[type="email"]{
 border: 1px solid blue;
}
[required]{
 color: red;
}
/* Seleccionar por atributos por */
/* Ccomienza por ^ */
/* Terminan con $ */
/* Contiene * */

/* Seleccionar por atributos  comienza por ^ */
/* Todos los atributos que comienzan por lo que le especificas, se le ponen las características */
a{
 color: blue;
}

[href^="/"],
[href^="https://ed"]
{
  color: red;
  background: none;
 }
 
/* Seleccionar por atributos  que terminan con $ */
[href$=".pdf"]{ 
 color: purple;
}

/* Seleccionar por atributos  que contiene * */
[class*="button-"]{ 
 color: purple;
}
```
[normalize.css](https://necolas.github.io/normalize.css/)
Los selectores son son case insensitive, depende donde se aplican en el HTML o XML:
* Tags: Son case **insensitive**
* Atributos: Son case **sensitive**
Si los escribimos igual en ambos sitios ahorramos problemas.

#### Especificad, herencia y cascada
```css

```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYwMTA0NTA0LDY0Mjk0ODg0NSwtODMzMz
I4Mzk3LDEyMzk4NTMyMzMsMTI2ODM3NzM5MSw1OTcyNzA3Nzgs
MTMzMTQwMzY4MSwtMTQ2NTI0NjE0MSwtNjA3MzM4OTQwLC0xND
A0MDU2NDcyLC0xMjIxMzE4ODMwLDIwNTExNDMwLC04ODUyODE5
MDUsLTE1MjYyMzM2NiwtNjE4Nzc1OTYxLDEzMzAyOTU1OTEsLT
kzMTE1NTA2MSwxNTIxNTExOTU5LC0xMjU0NDk3NzEyLC04NDgw
MjkwNjhdfQ==
-->