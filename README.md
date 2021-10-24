# hackathonbbva2021

## Problema a solucionar 

### Reto

* Buscar un modelo para incorporar la rentabilidad dentro del modelo de vinculación
* Modelo analitico que permita generar clusteres asociados a perfil de cliente y combinación de productos con miras a generar palancas de acción para maximizar la rentabilidad.

### Lo que queremos hacer:

* Usar métodos de clustering para separar los datos 
  https://dzone.com/articles/kmeans-silhouette-score-explained-with-python-exam

### Herramientas a usar

* Usando k-means
  K-means es uno de los métodos de clustering más utilizados. Destaca por la sencillez y velocidad de su algoritmo, sin embargo, presenta una serie de limitaciones que se deben tener en cuenta.
  
  Requiere que se indique de antemano el número de clusters que se van a crear. Esto puede ser complicado si no se dispone de información adicional sobre los datos con los que se trabaja. Se han desarrollado varias estrategias para ayudar a identificar potenciales valores óptimos de K (elbow, shilouette), pero todas ellas son orientativas.
  
  Dificultad para detectar clusters alargados o con formas irregulares.
  
  Las agrupaciones resultantes pueden variar dependiendo de la asignación aleatoria inicial de los centroides. Para minimizar este problema, se recomienda repetir el proceso de clustering entre 25-50 veces y seleccionar como resultado definitivo el que tenga menor suma total de varianza interna. Aun así, solo se puede garantizar la reproducibilidad de los resultados si se emplean semillas.
  Presenta problemas de robustez frente a outliers. La única solución es excluirlos o recurrir a otros métodos de clustering más robustos como K-medoids (PAM).

## Variables principales:

* Tenencias del producto:
  * saldo: Un mayor saldo es más conveniente.Representa un mayor volumen de negocio y una mayor ganancia por el importe en intereses que genera
* Rentabilidad el cliente:
  * ganancias y pérdidas
* Rentabilidad del producto:
  * Ganancias y pérdidas que se generan por cada producto que tiene el cliente
* Detalle tarjeta de crédito
  * Todos los movimientos
* Información RCC 
  * info de los dos productos que tiene un cliente


## Análisis de la base datos:

* CAMPO (Número de documento): no aporta valor, se puede obviar
* CAMPO(DEPENDIENTES, SITUACION_LABORAL, TIPO_EMPLEO, TIPO_PROFESION) 
