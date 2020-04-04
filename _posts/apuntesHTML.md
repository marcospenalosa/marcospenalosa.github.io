
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
Las etiquetas **< script >**  Se suele poner al final del body para evitar problemas al cargar los procesos java

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
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTM5MjEzMTAwLC03OTU5MTU3NTEsLTE4NT
UxMzUwMTYsLTE2MDQ1MTYzOTddfQ==
-->