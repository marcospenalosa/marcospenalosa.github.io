


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
   * Partes de un informe:
     *  Cabecera de página: Siempre
     *  Cabecera de informe: Al inicio del informe
     *  Cabecera de agrupamiento: Dentro del agrupamiento
	 * Detalle 1
	 * Detalle n
      * Pie de agrupamiento: Dentro 
      * Pie de informe: Al final del informe
      * Pie de página: Siempre 

<!--stackedit_data:
eyJoaXN0b3J5IjpbODU4MjIxNzM0LC03ODQ4MzYzMiwxNTA4OD
QxMTg0LDk0NjAyNTI4MywtMTc3NTQ5ODgzOCwtOTgyMjA0Mjg2
LC0yMjY5ODA1MzUsOTMxMDc3MTc3LDU1NzIxMDQzNCwxODIyMD
Y3MzU1LDE5NTI3MTg3OTYsLTExMjM0NDM5NTQsNTY4OTczMDg4
LDgzMDExOTMxOCwxNDgwNDgzMTg2LDQwNTg0MDc4NiwxMTI3OT
U2ODMyXX0=
-->