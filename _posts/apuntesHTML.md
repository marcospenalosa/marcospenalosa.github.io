
### Apuntes HTML

#### Sintáxis básica de un documento **HTML**
```html
<!DOCTYPE html>
<html lang="es">
	<head>
		<meta charset="utf-8">
		<title>Titulo</title>
	</head>
	<body>
	
	</body>
</html>
```

#### Sintáxis usual de un documento **HTML**
```html
<!DOCTYPE html>
<html lang="es">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<meta name="description" content="Una descripción de mi página">
		<title>Titulo</title>
		<link rel="stylesheet" href="sytles.css">
		<link rel="shortcut icon" href="favicon.png">
	</head>
	<body>
		<h1>Título de mi página web</h1>
		<script src="scipts.js"></script>
	</body>
</html>
```
* Las etiquetas **< script >**  Se suele poner al final del body para evitar problemas al cargar los procesos java
* Favicon: Tambíen se puede poner < link **rel="icon"** href="img/favicon.png">

#### Etiquetas de sección
```html

<header> Encabezado </header>
<nav>Barra de navegación</nav>
<article > Un post de un blog, por ejemplo
	<h1>Título</h1>
	<section> Divisiones 
		<h2>Subtítulo</h2>
	</section>
</article>
<aside> Contenido no relacionado con el article</aside>
<footer>Notas al pie</footer>
```
#### Listas
```html
<!-- UL no ordenadas, OL ordenadas -->
<ul>  
    <li>Item de lista 1</li>  
    <li>Item de lista 2  
    	<ol>  
            <li>Subitem de lista 1</li>  
            <li>Subitme de lista 2</li>  
        </ol>  
    </li>  
    <li>Item de lista 3</li>  
</ul>

<!-- Listas de definición -->
<!-- DL define la lista, DT un término, DD una descripción -->
<dl>  
    <dt>Perú</dt>  
    <dd>Lima</dd>  
    <dt>Colombia</dt>  
    <dd>Bogotá</dd>  
    <dt>Bolivia</dt>  
    <dd>Sucre</dd>  
</dl>

```
#### Otros elementos de la estructura
```html
<!-- Rompe el flujo del article, pero está relacionado, por ejemplo un artículo que en medio tiene una imagen -->
<figure>  
	<pre>
		<code>  
			function hola() {  
				return "hola"  
			}  
		</code>  
	</pre>  
    <figcaption> <!-- Es optional, es la descripción del figure --> 
    	Declaración de una función JavaScript.  
    </figcaption>  
</figure>

<!-- Elemeno principal -->
<main>  
	<p>Esto es un párrafo, es decir un bloque de texto.</p>  
    <hr>  <!-- Cambio de sección -->
    <pre>  <!-- El contenido se muestra tal cual está escrito -->
    	Este texto  
    		se representara igual  
    en el navegador  
    </pre>  
    <blockquote>  
    	Usa blockquote para destacar citas.  
    </blockquote>  
</main>

<!-- Divisiones (layout) -->
<div class="user">  
    <div class="user_name">  
        <p>Alexys Lozada</p>  
    </div>  
    <div class="user_image">  
        <img src="alexys.jpg" alt="Foto de Alexys Lozada">  
    </div>  
</div>
```
#### Tipos de elementos
```html
<p>Este es un elemento de bloque</p>   <!-- El siguiente elemento sale debajo -->
<span>Este es un elemento de línea</span> <!-- El siguiente elemento está a continuación -->
```
##### Elementos de línea
```html
<small>Texto legal</small>  
<strong>Texto importante</strong>  
<em>Énfasis</em>  
<cite>Citas</cite>  
<dfn>Definición</dfn>  
<code>Código</code>  
<data>Datos</data>  

<br>Saltos de línea  
<q>Citas</q>  
<abbr>Texto abrebiado</abbr>  
<del>Texto eliminado</del>  
<wbr>Ruptura de palabras  
<span>Contenedor de texto</span>  
<i>Itálica</i>  
<b>Negrita</b>  
<u>Subrayado</u>  

<sup>Superíndice</sup>  
<sub>Subíndice</sub>  
<time>Horas o Fechas</time>  
<mark>Texto resaltado</mark>  
<a href="">Enlaces</a>
<a target="_blank">Abrir una nueva página.</a>
```
##### Marcadores
```html
<ul>  
    <li><a href="#infancia">Ir a Infancia</a></li>  
    <li><a href="#juventud">Ir a Juventud</a></li>  
    <li><a href="#exito">Ir a Éxito</a></li>  
</ul>  
  
<h2 id="infancia">Infancia</h2>  
<h2 id="juventud">Juventud</h2>  
<h2 id="exito">Éxito</h2>
```
#### Imágenes
```html
  
<img src="https://images.pexels.com/photos/341372/pexels-photo  
341372.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="foto de una novia">  

<img src="imagenes/foto_novia.jpeg" alt="foto de una novia">
```
Fotos Gratis Libres de Derechos de Autor: [Pexels](https://www.pexels.com/es-es/)  
Mundo de los Gifs: [Giphy](https://giphy.com/)

**viewport** Cantidad de píxeles que *reales* que tiene el dispositivo (el tamaño, un móvil FHD no tiene 1920x1080 píxeles reales) -> **devicePixelRatio** nos dice el número de píxeles que hay por cada pixel real.

```html
<img src="img/bride.jpg"
srcset="img/man.jpg 1.2x,
	img/dogs.jpg 2x">
<img src="img/bride.jpg"
srcset="img/man.jpg 500w,
	img/dogs.jpg 800w">
```
**srcset** nos permite cambiar la foto según el devicePixelRatio, width (tamaño de la pantalla)

```html
<picture>
	<source srcset="img/dogs.jpg" media="(min-width: 800px)">
	<source srcset="img/man.jpg" media="(min-width: 500px)">	
	<img src="img/bride.jpg"
alt="Foto de una novia">
</picture>
```
**picture** obtenemos el mismo resultado, hay tener cuidado con los source, en cuanto se cumpla uno no evalúa el resto.

#### Microdatos y Open Graph
[schema.org; define los estándares de microdatos](schema.org)
```html
<div itemscope itemtype="http://schema.org/Movie">
  <h1 itemprop="name">Avatar</h1>
  <span>Director: <span itemprop="director">James Cameron</span> (born August 16, 1954)</span>
  <span itemprop="genre">Science fiction</span>
  <a href="../movies/avatar-theatrical-trailer.html" itemprop="trailer">Trailer</a>
</div>
```
**itemscope itemtype**="http://schema.org/Movie" se ponen en el padre del elemento, puede ser un *div*, *article*, etc.
[Hta de pruebas de datos estructurados](https://search.google.com/structured-data/testing-tool/u/0/?hl=es)

[Open graph (protocolo de Facebook)](ogp.me)
```html
<html prefix="og: http://ogp.me/ns#">
<head>
<title>The Rock (1996)</title>
<meta property="og:title" content="The Rock" />
<meta property="og:type" content="video.movie" />
<meta property="og:url" content="http://www.imdb.com/title/tt0117500/" />
<meta property="og:image" content="http://ia.media-imdb.com/images/rock.jpg" />
...
</head>
...
</html>
```
También lo hay para twitter --> < meta property="twitter:image" >"

Se pueden buscar hta. para comprobar el funcionamiento.

#### Tablas

```html
<table>
<caption> Horario de clases</caption> <!-- Título de las tablas -->
<colgroup> <!-- Para seleccionar columnas -->
 <col>
 <col>
 <col>
 </colgroup>
  <thead> <!-- Si se usa encabezado-->
  <tr> <!-- Table row-->
   <th>Lunes</th> <!-- Table heading-->
   <th>Martes</th>
   <th>Miercoles</th>
  </tr>
  </thead>
 <tbody>
  <tr>
   <td>HTML</td> <!-- Table data-->
   <td>CSS</td>
   <td>JavaScript</td>
  </tr>
 </tbody>
 <tfoot>
  <tr>
   <td>6 créditos</td>
   <td>3 créditos</td>
   <td>2 créditos</td>
 </tfoot>
</table>

<!-- <td rowspan="2"></td> -->
<!-- La celda ocupa dos filas-->

<!-- <td colspan="5"></td> -->
<!-- La celda ocupa cinco columnas-->

<!-- Se suele poner al inicio de la tabla -->
<!-- Se suele poner tantos col como columnas -->
<!-- Pero si queremos actuar en una enconcreto -->
 <colgroup> 
 <col span="2">
 <col style="background: yello">
 </colgroup>
 <!-- Actuamos en la 3 columna -->
```

#### Formularios

```html
<!-- action -> archivo donde va actuar -->
<!-- <form action=""> -->
<form>
 <!-- Hay dos formas de poner los label -->
 <label for="nombre">Ingrese su nombre</label>
 <input id="nombre">
 
 <label>
  Ingrese su nombre
  <input>
 </label>
 <button>Enviar</button>
</form>

<form>
<!-- El atributo name nos indica donde van los datos en el backend -->
 <label>
  Ingrese su contraseña
  <input type="password" name="password">
 </label>
 <!-- <input type="subit"> para sustituir el bóton-->
 <!-- el atributo value es el texto a mostrar -->
 <input type="submit" value="Iniciar sesión">
</form>

<!-- con placeholder ponemos dentro del cuadro el texto que queremos -->
<input placeholder="Ingrese su nombre">
<!-- con required indicamos que es obligatorio -->
<input required>
<!-- con readonly indicamos que es solo lectura -->
<input readonly>

<!-- <input type="text"> -->
<!-- Hay muchos tipos de inputs. -->
<!-- text, password, email, date, number,...  -->
<!-- checkbox, radio,...  -->
<!-- para opciones únicas radio y el mismo atributo name para todos los radio  -->
<!-- Agrupar campos -->
<fieldset>
 <legend> Tus datos personales </legend>
</fieldset>

<!-- Lista de opciones -->
<select name="country" id="conuntry">
<optgroup label="Europa">
 <option value="Spain">España</option>
 <option value="France">Francia</option>
</optgroup>
<optgroup label="América">
 <option value="Colom">Colombia</option>
 <option value="Per">Perú</option>
</optgroup>
</select>  
<!-- <select name... id... multiple (permite con control pulsado seleccionar varias opciones -->

<textarea name="mensaje" id="" cols="30" rows="10" placeholder="Escribe tu mensaje">
</textarea>
```
#### Multimedia

```html
<!-- codec más usado H.264 -->
<!-- El atributo controls añade los botones -->
<video src="media/clase.mp4" controls ></video>
<!-- Atributos -->
<!-- autoplay -->
<!-- poster="img/poster.jpg"  le pones una imagen antes de reproducirlo -->

<audio src="" controls></audio>
<!-- reproductores video.js, flowplayer -->
```

#### Interactividad y contenido embebido

```html
<!-- Muestra una flecha desplegable -->
<details>
 <summary>Título</summary>
 <p>Texto</p>
</details>

<!-- Muestra una "cuadro" por encima de todo, es un modal -->
<dialog id="modal">
  <p>Texto</p>
</dialog>
<!-- para mostrarlos se usa un script, puede ser cualquier cosa, no solo un boton -->
<button id="button">Abrir modal</button>
<script>
 const modal = document.getElementById('modal');
 const button= document.getElementById('button');
 button.addEventListener('click', () => {
 modal.setAttribute('open', 'true')
 })
 </script>
<iframe width="" height="" src="">
<!-- Trae una página dentro del iframe -->
</iframe>
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNTkzMTc2NjYsLTIxMTE4NjE4OTUsLT
gwNjQ1NjU1OSw1ODU1NzQ5MzAsLTE1NjgyOTI1NjAsMTI3MzIy
MzA3NCwtOTc4MjI1ODI0LDEzNzM5Mjc3NTAsMjA3NzI4MDcwOS
wyNzgyMTE0MTYsMjAzOTIxMzczNSwtMTE5NzExNTE2MywyMTUz
NDI2ODQsNjY3NzczNzYzLC03NDYxNjgyOTksNjUxOTU5MTAxLC
03ODgzMDI4MzUsLTE0MDAyNTM0NzAsLTMzMTg4NjkzLC0xMjU3
OTAwOTg3XX0=
-->