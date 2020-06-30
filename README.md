# Tarea3: Trabajo escrito: Luis Diego Segura Ureña B66781
Lo primero que se hizo fue modofocar el archivo xy.csv, donde se quitó la columna correspoondiente a Xn, para facilitar el trabajo a futuro.

#Parte 1: En el archivo "Ajuste de marginales"
Primero buscamos calcular la función de densidad marginal de X y de Y.
Para ello haremos uso de los datos de xy.cvs
Hacemos un vector que represente la matriz marginal X, para esto haremos la sumatoria de las filas de xy.cvs, para ello usamos panda, con pd.DataFrame podemos trabajar un vector con pandas. para sumar las filas se usa .sum(axis=1)
Para encontral los valores marginales de Y usar la misma función de pandas, ahora con .sum(axis=0) para que se sumen las columnas.
Usando np.linspace, se crea un espacio vectorial para graficar las marginales 
Se establecen nuevas matrices: fx y fy
gráficamos X por un lado y Y por el otro y a cada una le superponemos una gráfica que será la el "ajuste"
el ajuste queda dado por una gaussinana por medio de sns.distplot

#Parte 2: En el archivo "Densidad conjunta"
Se definen los vectores necesarios como en la parte 1
Ahora definimos nuevos vectores con pandas usando pd.DataFrame
Ojo con "ypanda" el cual hay que recortar para que sea del mismo tamaño que "xpanda"
Hacemos la multiplicación de los dos vectores, dando como resultado un nuevo vector "Mxy", contiene los datos de la densida conjunta, lo transformamos en un array definido como "F"

#Parte 3: Archivo "Parte 3"

Correlacion:
Ya con los vectores definidos, porcedemos a calcular la coorelación, para ello primero definimos los vectores con Y, X, y XY(donde XY es la matriz xy.cvs) un array.
Definimos el la fomula de correlación, en mi caso lo hice paso por paso, por eso fue necesario definir los array anteriromente para aprovechar cada elemento de las matrices. La ecuación se presenta un poco compleja pero cumple la misma función de sumatorias de productos. 
Definimos el resultado de la correlación como "Rxy"

Covarianza:
Primero calculamos las medias de X y Y con la función .mean().
Según la fórmula la covarinza depende de la correlacion dividida por el producto de las medias 
Queda definido el resultado como "Cxy"

Pearson:
Para Pearson se hace uso de la varianza mediante la función .var(), al sacar la raiz cuadrada de la varianza tenemos la desviación estandar
Pearson queda definido como la covarianza dividido entre el producto de las desviaciones estandar
El resultado queda definido como "P"

#Parte 4: Para las gráficas de las marginales está el archivo "Gráficas Marginales" y para la densidad conjunta ver archivo "Densidad Conjunta"

Para las marginales, se definió una serie de vectores, para x desde x5 hasta x15; para y desde y5 hasta y25
Haciendo el uso de los vectores X y Y antes definidos, los usamos como componestes a graficar, X con sus respectivos xn, y Y(se usa un Yp que eson los elementos deseados, que se filtraron de Y) con sus yn.
Se grafican respectivamente

Para la densidad conjunta, es continuar lo explicado en la parte 1, nada más es cuestión de graficar los datos.

