


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
   
### vReport e Informes
* Se puede editar desde 2 sitios:
  * vDevelop: 
* Partes de un informe:
   *  Cabecera de página: Siempre
   *  Cabecera de informe: Al inicio del informe
   *  Cabecera de agrupamiento: Al inicio del agrupamiento
       * Detalle 1
	* Detalle n
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
eyJoaXN0b3J5IjpbLTE3MjA2NDQ0ODEsLTE1MTE0Nzg3MjMsLT
I4ODE3NjA1MywtNzg0ODM2MzIsMTUwODg0MTE4NCw5NDYwMjUy
ODMsLTE3NzU0OTg4MzgsLTk4MjIwNDI4NiwtMjI2OTgwNTM1LD
kzMTA3NzE3Nyw1NTcyMTA0MzQsMTgyMjA2NzM1NSwxOTUyNzE4
Nzk2LC0xMTIzNDQzOTU0LDU2ODk3MzA4OCw4MzAxMTkzMTgsMT
Q4MDQ4MzE4Niw0MDU4NDA3ODYsMTEyNzk1NjgzMl19
-->