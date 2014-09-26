# Notas
Se agrega la versión inicial.

## Cambios

#### Corrección de la Macro inicial. *Listo*.
Cuando se abre el libro, sobre-escribe los valores iniciales, pero no discrimina sobre la hoja en la que se hace, por lo que si no se cierra el libro en la cotización, se sobreescriben valores en otras hojas al momento de abrirse.

#### Agregar el tipo de auto 3.5T. *Listo*.
Para poder discriminar en las coberturas adicionales, se requiere este concepto.

#### Ajuste Cobertura Auto Substituto. *Listo*.
Permisible si el tipo de auto **no** es 3.5T.

#### Ajuste Cobertura Indemnización Valor Factura. *Listo*.
Cuando el tipo auto es 3.5T sólo se permite hasta el primer año.

#### Actualización de leyendas de seguro. *Listo*.
Eliminar *Generali* de las leyendas. 

#### Descuento por estado. *Listo*.
No aplica en 3.5T

#### Cobertura Premium. *Listo*.
Se calcula y aplica cuando  el tipo de auto **no** es 3.5T

#### Generar versión hasta este punto.

## Tipo Cliente
Agregar el concepto de Tipo Cliente. Hasta ahorita, el tipo cliente pudiera clasificarse como "Nuevo" o "Estándar".

Hay otro tipo que debemos soportar, que es el "Nominahabiente o Recurrente"

Los cambios importantes de este nuevo concepto, es que la Comisión por Apertura depende del Tipo de Cliente. Para el "Estándar", es de 2.5% y para el "Recurrente" es del 1%.

Además, Las Tasas de Interés, y los rangos para Tipo de Tasa también son diferentes para cada Tipo de Cliente.

Las condiciones para determinar el Tipo de Tasa "Tasa Ordinaria" o "Tasa Reducida" también son dependientes de esta figura:

* Estándar: Monto a Financiar >= $200,000 O enganche >= 30%
* Recurrente: Monto a Financiar >= $200,000 O enganche >= 25%

Para Autos Seminuevos, la selección del Tipo de Tasa es similar para ambos Tipos Cliente: sólo se considera el enganche, que sea >= 35%

Posteriormente se discrimina por Plazo para hallar la tasa de interés específica final.

## Cobertura adicional Mujer Banorte

####Descripción
Permisible cuando el Tipo Persona **no** es Moral, y el tipo de auto **no** es 3.5T.

* Catálogo Si/No.
* Depende del Estado.
* Aplica Factor Multianual.
* Forma parte de la Prima de Daños.

