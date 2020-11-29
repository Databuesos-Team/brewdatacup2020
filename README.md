# Brewdatacup2020

Participación en la [Brewing Datacup 2020](https://www.brewingdatacup.com) por Juan Javier Santos Ochoa y Jorge Juvenal Campos Ferreira.

## Instrucciones. 

Para ejecutar el modelo realizado por el equipo durante el Datatón, hay que descargar los archivos que componen el presente repositorio. 

## Software requerido. 

* Python 3.0 o más reciente. 

* Una instalación de `Jupyter Notebook` instalada en el ordenador. 


## Descripción del problema

1. Existencia de 3,625 puntos de demanda de producto. 

2. La frecuencia de entrega para estos puntos es variable, variando desde 1 entrega a 3 entregas a la semana. 

3. El volumen de demanda por parte de las tiendas es variable. 

4. Las entregas que se lleven a cabo en los distintos centros de distribución deben **estar balanceadas**, es decir, por motivos de logística, las entregas llevadas a cabo a lo largo de la semana tienen que ser lo más similares posible en distancia recorrida, volumen de producto entregado y número de paradas realizadas. 


## Modelo utilizado. 

Se utilizó un ensamble de modelos de Machine Learning de clustering para la clasificación de zonas de venta de cerveza, combinado con Programación Lineal. 

Los modelos de ML y PL utilizados fueron: 

1) Clustering con k-means. 

2) Corrección de clustering en las fronteras utilizando el algorítmo de k-Nearest Neighbors. 

3) Introducción de restricciones de balanceo a través del módulo de Python `pulp`, para forzar las condiciones de balanceo en la formación de los clusters de repartición. 

