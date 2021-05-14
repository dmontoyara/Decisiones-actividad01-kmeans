# Decisiones-actividad01-kmeans


# Planteamiento del problema

El propósito central del experimento es analizar un agrupamiento de datos cuando existe un solapamiento entre ellos. Es decir, los datos a simple vista no son fácilmente clasificables con un modelo matemático. Las limitaciones de los modelos matemáticos habituales para clasificar, ponen en marcha alternativas que discriminan de forma aproximada y con buenos resultados en la práctica.

Otra problemática es la presencia de la correlación en el agrupamiento de datos. Al ingresar variables adicionales que dependen de otras que se encuentran previamente en el modelo, se tiene la hipótesis que los centroides de agrupamiento puedan verse afectados y no se estabilice correctamente. Con la inicialización aleatoria del método, es importante controlar la semilla o la cantidad de iteraciones con las que empieza a generar el agrupamiento.


# Descripción de la metodología

La metodología implementada en la solución de la actividad fue Kmeans, esta técnica es una algoritmo de clasificación no supervisada o clustering que usa la distancia de las observaciones a un centroide definido para determinar su pertenencia al grupo dado por dicho centroide, la definición de la cantidad de grupos (definición del parámetro k) a encontrar por el algoritmo, se realiza previamente a la inicialización de kmeans, una de las técnicas para definir esta cantidad de grupos es la gráfica de codo o en ingles Elbow method. Los pasos usados por kmeans son:

        * Selección de k centroides (esta selección se realiza de manera aleatoria).
        * Asignación de las observaciones al centroide más cercano (usa distancia cuadrática).
        * Actualización de los centroides, una vez clasificado cada observación se promedian los valores de cada grupo formado y dicho promedio se convierte en el nuevo centroide.


# Resultados del Experimento:

Punto 1:
Se realizó una distribución adicional llamada "muestra 5", donde tiene un traslape frente a los otros dos conjuntos iniciales. Se utilizó un tamaño de muestra de 100 y un vector de medias de (-0.8, 1) para lograr dicho traslape.

Punto 2:
A partir de la definición inicial de las 3 distribuciones, se encontraron los centroides para 4 ejecuciones con 3 clusters, y se encontró que los centroides no varían en cada ejecución. En esta parte la única diferencia que se observa es que los clusters intercambian posiciones entre sí, aunque no afecta el resultado final.

Punto 3:
Al agregar una variable adicional como la suma de la primera variables y una distribución similar, se encuentra que la varianza se encuentra entre los valores 1.19 y 1.86. El valor de la covarianza entre x1 y x3 se encuentra entre 0.55 y 0.81. La estabilidad de los centroides no se observa cambiar en los resultados de las 4 ejecuciones.

Punto 4:
Los valores que se obtienen de los centroides no parecen cambiar entre sí a partir de 7 clusters. Únicamente cambia el orden en que se escogen los grupos, sin que esto afecte el resultado final.

Los valores cambiantes de los centroides responden a comportamientos dados por datos con valores extremos en ambas direcciones. con valores de varianza iguales para todas las distribuciones, la posición de los centroides no cambia.

# Bibliografía
Geeksforgeeks. (2021). Elbow Method for optimal value of k in KMeans. https://www.geeksforgeeks.org/elbow-method-for-optimal-value-of-k-in-kmeans/
MamutCola. (n.d.). Introducción a las técnicas multivariantes de clasificación. http://ares.inf.um.es/00Rteam/pub/mamutCola/modulo6.html
RPUBS. (2019). Matrices, Vectores y Escalares. https://rpubs.com/cete/fundamentosr3
Sitiobigdata. (2019). Covarianza y correlación: comprendiendo su utilidad. https://sitiobigdata.com/2019/10/26/covarianza-y-correlacion/#
SOLIN. (2017). MEDIA VARIANZA COVARIANZA REGRESIÓN LINEAL. http://www.solin.16mb.com/estadistica_js/VarianzaCovarianzaRegresion.htm
stat.ethz. (n.d.). Correlation, Variance and Covariance (Matrices). https://stat.ethz.ch/R-manual/R-devel/library/stats/html/cor.html
UNIOVIEDO. (n.d.). El algoritmo k-means aplicado a clasificación y procesamiento de imágenes. https://www.unioviedo.es/compnum/laboratorios_py/kmeans/kmeans.html
Wikipedia. (n.d.). Matriz de covarianza. https://es.wikipedia.org/wiki/Matriz_de_covarianza
(UNIOVIEDO, n.d.)(Geeksforgeeks, 2021)
El algoritmo k-means aplicado a clasificación y procesamiento de imágenes https://www.unioviedo.es/compnum/laboratorios_py/kmeans/kmeans.html
Elbow Method for optimal value of k in KMeans https://www.geeksforgeeks.org/elbow-method-for-optimal-value-of-k-in-kmeans/
