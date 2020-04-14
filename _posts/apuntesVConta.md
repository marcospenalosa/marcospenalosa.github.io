# Apuntes vConta

* En vConta hay **entidades**, luego se declarael tipo (*cliente*, *proveedor*, *ambos*, etc)
  *  Tabla ENT (contacto)
    *  Tabla DIR: Dirección (hay de teléfonos, emails...)
    *  Tabla ENT_ENT_TIP: La unión de tipo y entidad
      *  Tabla ENT_TIP: Son los tipos que hay.
      * También hay ENT_AGR **(Comprobar nombre)** que para el mecanismo de asignar el N_NUM a los ENT_ENT_TIP es decir tengo un ENT_TIP Cliente (CLT) y otro Cliente Potencial (CLP) pero quiero que cuando los vaya dando de alta el contador de su n_num sea el mismo entonces se crea una agrupación de CLT y CLP.
      
Luego existen ENT_REL y REL_TIP: Zara Bershka Pull&Bear están relacionados con Inditex, la relación es que son del mismo grupo.
* **Siempre** hay que crear una cuenta auxiliar aunque no sea necesario. ("*129.1*")
  * Se pueden virtuarlizar cuentas 
* Asiento: Qué operación se hace.
  * Apunte: Dónde afecta esa operación.
    * Compensación: cancelar un apunte (generar el cargo/gasto o el abono/pago)
    * *Cobro* vivo: apuntes de la cuenta *Deudor* o *Acreedor* **sin** compensar (pagos y cobros **sin** realizar) .
    * Saldo vivo: El estado actual de una *entidad* con la empresa.
    * *Pago* vivo: apuntes de la cuenta *Proveedor* **sin** compensar (pagos **sin** realizar) .
* Modelos:
  * 303 : IVA.
  * 340: Operaciones realizadas (facturas).
  * 349: Operaciones intracomunitarias.
  * 115: IRPF.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4NzM0Mjg3MywyMDIwODUyOTQzXX0=
-->