
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
````html
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

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MzgzOTM3NzcsMTA4MDI3OTQsLTc1ND
YwNTcxOCw2OTQyODQxNzQsOTIyNDM4MDgxLDkzOTIxMzEwMCwt
Nzk1OTE1NzUxLC0xODU1MTM1MDE2LC0xNjA0NTE2Mzk3XX0=
-->