# Dashboard analítico de Restaurante

Este fue un ejercicio realizado y ejecutado a partir de las instrucciones dadas, en el curso de Power BI de la academia de aprendizaje 'A2 Capacitación'.

En este dashboard encontramos información referente a las ventas y la distribución de ellas en el entorno de un restaurante, tales como.
    - Propinas por mesero
    - Ventas por comida o bebida
    - Ventas a lo largo del tiempo
    - Informe de ventas por sucursal
    - Análisis de ventas por mesero

El archivo está dividido en cinco secciones en donde encontrarás:
    - Portada
    - Sucursales
    - Análisis de órdenes
    - Órdenes 
    - KPI's

## Portada

Esta sección fue diseñada con la finalidad de tener un panorama amplio del comportamiento de ventas del restaurante.

Encontramos las 'Ventas Totales' hasta el corte del archivo de origen proporcionado. 

Para el resumen de ventas se utilizó el gráfico de tarjeta (card) y se agrupó la informción con la función de 'sum' para tener el datol total de ventas.

Por otro lado se agregó un 'Multi-row card' con la finalidad de utilizar dos campos y agrupar las ventas por categoría:
    - Comida
    - Bebida
Y así tener de cada una de estas categorías la cantidad total indivualizada de las ventas correspondientes. 

A continuación utilicé 'Stacked column chart' con la finalidad de visualizar la distribución de ventas que tuvo el restaurante a través de los meses.

Para esta visualización se utilizó una medida creada con 'DAX'

    - Ventas YTD = TOTALYTD([Ventas totales],Detalles1[Fecha].[Date])

Esta medida fue de utilidad puesto que el archivo utilizado contiene tres tablas, pero para poder hacer uso de ellas es necesario crear las relaciones entre tablas.

Es decir en una tabla de hechos tenemos todos los datos de las ventas y por otro lado tenemos una tabla calendario donde tenemos qué productos por categoría se vendieron en qué fechas del año.

Para lograr la unión de las dos tablas se creó esa medida de DAX.

Finalmente en la Portada tenemos un gráfico de 'Línea del tiempo' en la que nos explica como han ido cambiando las ventas a través de los meses, días o años. 

Esta gráifica hace un recuento de ventas por fecha, es decir, cuanto vendimos en determinado día y cómo ha ido cambiando durante el tiempo.

## SUCURSALES