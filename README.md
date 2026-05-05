# EDA Electricity Transformer Dataset (ETDataset)

## Justificación
Este EDA ha sido elaborado para la realización de la práctica sobre Redes 
Neuronales Recurrentes para la asignatura de Deep Learning del Máster en Ciencia
de Datos por la Universidad Oberta de Catalunya.

## Insights del EDA

Atendiendo la gráfica de correlación, solo existe correlación entre las temperaturas HUFL (High UseFul Load) y MUFL (Middle UseFul Load),
y HULL (High UseLess Load) y MULL (Middle UseLess Load). Esto tiene sentido porque es probable que al ir aumentando la carga útil o inútil 
pase de Middle a High.

Atendiendo a los gráficos separados por temporalidad (año, mes, día y hora) vemos que el mayor cambio está en la hora, en concreto en las 
MUFL y HUFL (que hemos visto que están correlacionadas, por lo que tiene sentido que ambas cambien en base a la hora).

Siguiendo con la temporalidad, en concreto en los meses, vemos que el gráfico de la variable objetivo (OT) cambia significativamente 
en los meses de verano, cuando hay más temperatura ambiente.

Anualmente, se ve que la variable objetivo baja consecutivamente su rango.

Por último, en cuanto a los días, se ve que la variable OT aumenta al final del mes.

Otros aspectos que se tienen en cuenta en el EDA es la carencia de nulos, lo cual facilita la gestión de procesado. Además, la columna 
fecha tenía formato object, por lo que se tuvo que hacer un df temporal, cambiando la variable a datetime, para poder hacer la 
separación de la temporalidad.
