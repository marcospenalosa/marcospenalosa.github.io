


### Paso básicos a la hora de crear una aplicación en Velneo
### Crear el proyecto
* Creamos el proyecto con la opción datos e interfaz.
  * Añadir el alias = que el nombre.
  * Añadimos los dibujos de las tablas (iconos).
 
### Creamos las tablas
* Creamos las tablas desde el editor de esquemas.
  *  El enlace plural se hace desdel maestro a muchos.
     * Una familia puede tener muchos artículos.
     * A través de la línea **azul** puede *obtener* los datos de la familia
     *  A través de la línea **roja** puede *cargar* los artículos
   * Los campos **indirectos*** ***reales*** se usan para apuntar a tablas que no están directamente relaciondas y queremos **actualizar los registros**.
     * Se tiene que resolver un índice único.  
   * * Los campos **indirectos*** ***virtuales*** se usan para apuntar a tablas que no están directamente relaciondas y solo queremos **leer los registros**. 
   * 
### Interfaz
* Solo puede haber un marco AUTOEXEC, que puede ser herado y es donde se indica el formulario de inicio.
* Para que se pueda avanzar con ENTER dentro del formulario:
   *  Creamos un botón de alto y ancho 0.
   *  Lo ponemos como *botón por defecto*
   *  Comando --> Mover foco al control siguiente
 * Menú -> Acciónes (los botones).  
 * Rejilla --> Editable cuerpo verdadero (permite editar directamente los datos)
 * [Video 77](https://www.youtube.com/watch?v=-1NGm5foTdo&list=PL-bVpgNOlmioFuAHHTmRlXX2dlof9w_tY&index=77) --> Como hacer un informe 
   
### Programación 
   * Shift + F4 --> Abre el asistente de programación.
   * Funciones de **campo**:
     *  #FCH **:** isModified() --> Comprueba si un campo ha cambiado
   * Shift + F6 --> Comenta las líneas seleccionadas.
   
### vReport
* Se puede editar desde 2 sitios:
  * vDevelop: Objetos -> Editar informe externo.
  * vClient: Es la mejor opción, porque se ve los cambios en directo, mediante comandos.
* Partes de un informe:
   *  Cabecera de página: Siempre
   *  Cabecera de informe: Al inicio del informe
   *  Cabecera de agrupamiento: Al inicio del agrupamiento
       * Detalle 1
       * Detalle N
* Pie de agrupamiento: Al final del agrupamiento
* Pie de informe: Al final del informe
* Pie de página: Siempre .
* En vReport siempre tenemos que ordenar la lista que le pasemos. 
* Definir impresora lógica.
   *  Path: usuario/velneo/printers/vrl
    * Extensión del fichero: **.vil**
 *  Modos de impresión:
     * Impresora.
     * Disco.
     * Pantalla. 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk2NTQzNTc2LC00NTQyODQ4OTUsNDExNz
YzMTczLC0xNTExNDc4NzIzLC0yODgxNzYwNTMsLTc4NDgzNjMy
LDE1MDg4NDExODQsOTQ2MDI1MjgzLC0xNzc1NDk4ODM4LC05OD
IyMDQyODYsLTIyNjk4MDUzNSw5MzEwNzcxNzcsNTU3MjEwNDM0
LDE4MjIwNjczNTUsMTk1MjcxODc5NiwtMTEyMzQ0Mzk1NCw1Nj
g5NzMwODgsODMwMTE5MzE4LDE0ODA0ODMxODYsNDA1ODQwNzg2
XX0=
-->