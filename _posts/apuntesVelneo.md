


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
   *  Cabecera 
      * De página: Siempre
      * De informe: Al inicio del informe
      * De agrupamiento: Al inicio del agrupamiento
         * Detalle 1
         * Detalle N
  * Pie 
    * De agrupamiento: Al final del agrupamiento
    * De informe: Al final del informe
     * De página: Siempre .
* En vReport siempre tenemos que ordenar la lista que le pasemos. 
* Definir impresora lógica.
   *  Path: usuario/velneo/printers/vrl
    * Extensión del fichero: **.vil**
 *  Modos de impresión:
     * Impresora.
     * Disco.
     * Pantalla. 
  * En el editor de informes:
    * Marcar el check de Fichero -> Preferencia -> Miscelánea -> Abrir ventana maximizada
    * Informe -> Configuración de informe y página  
       * Modo de pasa doble: Si queremos hacer 1 pág de 50 hay que marcar este check para que vReport cuente cuantas páginas hay.
       * Opciones de sección: Se define las cabeceras y pies.
       * Origen de datos: Indicamos donde coge los datos.
          * Tablas y campos con check privados nos ayuda a quitar opciones a editar por parte del cliente.
        * Configuración de detalle: 
           * Si hay más de un detalle, se imprimen todos los registros del primer detalle, luego del siguiente... 
           * Agrupamientos: Sirven para juntar datos, los artículos de un cliente por ejemplo.
         * Secciones: Importante marcar el check de **Alto autómatico** 
         * Zonas: Separaciones verticales dentro de la misma sección.
 * Fórmulas script:
    * "$D{#NAME}" == "name" 
    * "Página " + $V{pageno} + " de " + $V{pagecount}
    * Con $P es para parámetros.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ4NDM1MTkxNSwtMTg5NTQxMjc0MCw2Mz
E4MTIyODIsMzg1NzQ0MTYzLC0xMDMyNTEyODM3LC0yMDE2MDQw
MTQ4LC00NzE4NDAyNzAsLTQ1NDI4NDg5NSw0MTE3NjMxNzMsLT
E1MTE0Nzg3MjMsLTI4ODE3NjA1MywtNzg0ODM2MzIsMTUwODg0
MTE4NCw5NDYwMjUyODMsLTE3NzU0OTg4MzgsLTk4MjIwNDI4Ni
wtMjI2OTgwNTM1LDkzMTA3NzE3Nyw1NTcyMTA0MzQsMTgyMjA2
NzM1NV19
-->