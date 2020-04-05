
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
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDIxNDM3MzE5LDkyMjQzODA4MSw5MzkyMT
MxMDAsLTc5NTkxNTc1MSwtMTg1NTEzNTAxNiwtMTYwNDUxNjM5
N119
-->