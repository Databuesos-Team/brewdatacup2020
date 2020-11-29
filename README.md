# Brewdatacup2020

Participación en la [Brewing Datacup 2020](https://www.brewingdatacup.com) por Juan Javier Santos Ochoa y Jorge Juvenal Campos Ferreira.

## Instrucciones. 

Para ejecutar el modelo realizado por el equipo durante el Datatón, hay que descargar los archivos que componen el presente repositorio. 

## Software requerido. 

* Python 3.0 o más reciente. 

* Una instalación de `Jupyter Notebook` instalada en el ordenador. 


## Descripción del problema

El objetivo es generar un modelo original, escalable y con lógica de negocio que permita proponer un esquema de logística para la repartición de producto proveniente de un Centro de Distribución Regional a lo largo de una semana. 

Las restricciones presentadas en el conjunto de datos son las siguientes: 

1. Existencia de **3,625** puntos de demanda de producto. 

2. La **frecuencia de entrega para estos puntos es variable**, variando desde 1 entrega a 3 entregas a la semana. 

3. El **volumen de demanda de producto por parte de las tiendas es variable.** 

4. Las entregas que se lleven a cabo en los distintos centros de distribución deben **estar balanceadas**, es decir, por motivos de logística, las entregas llevadas a cabo a lo largo de la semana tienen que ser lo más similares posible en _distancia recorrida_, _volumen de producto entregado_ y _número de paradas realizadas_. 

## Modelo utilizado. 

Se utilizó un ensamble de modelos de Machine Learning de clustering para la clasificación de zonas de venta de cerveza, combinado con Programación Lineal. 

Los modelos de ML y PL utilizados fueron: 

1) Clustering con k-means. 

2) Corrección de clustering en las fronteras utilizando el algorítmo de k-Nearest Neighbors. 

3) Introducción de restricciones de balanceo a través del módulo de Python `pulp`, para forzar las condiciones de balanceo en la formación de los clusters de repartición. 


# Resultado obtenido

Se obtuvo un modelo con los siguientes resultados: 

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> Dia </th>
   <th style="text-align:right;"> No. Paradas </th>
   <th style="text-align:right;"> Volumen repartido </th>
   <th style="text-align:right;"> Distancia </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> D1 </td>
   <td style="text-align:right;"> 666 </td>
   <td style="text-align:right;"> 9247.000 </td>
   <td style="text-align:right;"> 7124 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> D2 </td>
   <td style="text-align:right;"> 656 </td>
   <td style="text-align:right;"> 8886.000 </td>
   <td style="text-align:right;"> 5799 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> D3 </td>
   <td style="text-align:right;"> 650 </td>
   <td style="text-align:right;"> 9246.667 </td>
   <td style="text-align:right;"> 7234 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> D4 </td>
   <td style="text-align:right;"> 676 </td>
   <td style="text-align:right;"> 8886.833 </td>
   <td style="text-align:right;"> 7493 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> D5 </td>
   <td style="text-align:right;"> 653 </td>
   <td style="text-align:right;"> 9247.500 </td>
   <td style="text-align:right;"> 6019 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> D6 </td>
   <td style="text-align:right;"> 676 </td>
   <td style="text-align:right;"> 8886.000 </td>
   <td style="text-align:right;"> 7607 </td>
  </tr>
</tbody>
</table>






