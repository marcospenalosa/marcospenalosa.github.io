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

/* Seleccionar hermanos siguientes ~ */
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

#### Especificidad, herencia y cascada
Especificidad -> Se calcula en el selectores 
* tags 1
* clases 10
* id 100
* inline 1000
* !importan -> gana a todos  (no se debería usar)
Donde más sumen es la regla que se aplica.
Lo mejor es un usar un solo nivel con la ayuda de clases.

Cascada
Lo que viene después sobreescribe a lo anterior (a igual especificidad).

Herencia
Los hijos heredan las propiedades de los padres.

initial -> Obliga a resetear un elemento a un valor inicial
inherit -> Obliga a un elemento a heredar una propiedad.

```css
/* Obligo a "a" heredar el color si está dentro de p */

p{color: blue;}
a{color: inherit;}

/* Obligo a coger un color por defecto */
a{color: initial;}
```
#### Box model
Layout -> geometría de cada elemento (tamaños, posción, separación...)
Los elementos de línea no tiene height, width, margin, padding propios (por ejemplo <span>)
```css
h1 { display: inline;} /* Obligo al alemento a ser de línea */
span{ display: block;} /* Obligo al elemnto a ser de bloque */
/* display: inline-block;  lo hace de línea con heigh,width...*/
/* display: none; lo oculta a la vista */
```
Box model es algoritmo como el navegador interpreta el css.
* Content
  * Width
  * Height 
* Padding box
  * Padding 
* Border
  * Border 
* Margin
  * Margin
Box sizing, propiedad para cambiar la forma en que suma el total de la caja
```css
.box{
 width: 500px;
 height: 300px;
 box-sizing: border-box;
}
 /* Calcula la suma de la caja hasta el borde con el width y height que declaremos --> 500x300 en el ejemplo */
```
Se recomienda poner en la hoja de estilos css lo siguiente:
```css
*, *::before, *::after{
 box-sizing:border-box;
}
/* Así las cajas siempre tendrán la medida que indicamos */
```
* Margin
  * margin- top
  * margin-right
  * margin-bottom
  * margin-left
  * margin: 50px 100px 200px 30px; (top - right - bottom - left)
  * margin: 50px 100px; (top - bottom | right - left)
  * margin: -100px; ( a todo) (se pueden márgenes negativos)
  * Para centrar un elemento.
    * margin-left: auto;
    * margin-right: auto;
  
Colapsado de márgenes (solo ocurre de manera vertical), si tengo un article y un h1 dentro, el h1 manda en el margen y deja una separación, para ello hay que poner un padding-top:0.1px;

Las buenas prácticas dicen que solo se usen en una sola dirección y lo mejor es **margin-bottom**. Si hay un margin-top y un margin-bottom en otro elemento no se suman.

Padding: Si se usa porcentaje, utiliza el width del padre para calcular el tamaño.
**Tip para videos responsive**
```css
.video{
 padding-bottom:56.25% (16:9)
}
```
height:  50vh; 
width: 100vw;
vh y vw -> viewportHeight viewportWidth ( 50 % de la pantalla , 100 %)

Si el alto es automático, al hijo no se le puede aplicar un alto con porcentaje.

#### Bordes y sombras
Propiedades:
```css
.box{
 border: 100px solid black;
 border-width: 100px;
 border-style: solid;
 border-color: black;
 border-radius: 25px;
}
/*border-style: solid dotted dashed double*/
/* border-top, -right, -bottom, -left */
/* border-top-left-radius.... o border-radius:100px 50px 30px 25 px*/
/* border-top-left-radius: 100px 20px hace una elipse */
/* border: x x x x / y y y y; */
```
**outline** es una línea que se dibuja por fuera de la caja y se suele usar para inspeccionar el layout.
**Sombras** son la copia exacta del mismo elemento desplazado una distancia.
box-shadow: h-offset v-offset blur spread color | (inset -> se dibuja al lado opuesto)

```css
.box{
 box-shadow: 0 0 0 10px blue,
	     0 0 0 20px grenn;
	     0 0 0 30px yellow;
}
/* Creamos la sensación de múltiples bordes. */
box-shadow: -6px -px 40px rgba(0,0,0,.5) inset;
```

#### Fondos

```css
/* color siempre aparece debajo de imágenes */
background-color: yellow; 
background-image: url();
background-repeat: repeat | no-repeat | repeat-x | repeat-y;

/* Que parte de la caja cubrimos */
backgroun-clip: border-box | padding-box | content-box;

/* Desde que caja se crea el fondo */
background-origin: border-box | padding-box | content-box;

/* width calcula el alto | width height | contain - cover - auto */
background-size: 100px;
background-size: 100px 200px;
background-size: contain;
/* x -> y center | x y | x = left - center right <unit> / y = top - center - bottom <unit>
background-position: 50px;
background-position: 50% 50%;
background-position: right 20px bottom 20px;
/* Como se dibuja el fondo respecto al viewport */
background-attachment: 
```


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIyNTgxMDQwMSwtMTM5NzA3NzcxMSw3OT
QyODM4MzgsMTI2MTkwMzY3NiwtMTE4MjkzNDE4MCwxNTY0Njgx
MjQwLDI1NTY0MzY5OSwzMzE5NjYzODAsNDA5MDE3MjI4LC0xOT
U0NDY1NzgwLDIwNTUzOTE0NTQsNjgwMTgxNjMyLC03OTgxOTA1
MjgsNzgzMzMxNTgzLC02MDgzODkyLC0xMjA2NzY4ODU2LDEwMj
Y2MjQ4MjMsLTU3ODAwNzA1MiwxNjkwNTQ2MDAzLDcwOTgzNDQ0
NF19
-->