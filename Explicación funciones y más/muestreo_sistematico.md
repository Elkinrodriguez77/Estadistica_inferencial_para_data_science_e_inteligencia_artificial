Haz clic [aquí](../1.1%20Práctica%20funciones%20de%20muestreo.ipynb) para volver al notebook.


# 1. Función de muestreo sistemático (Paso a paso):

```python
def muestreo_sistematico(df,step):
    indices = np.arange(0, len(df), step=step)
    muestreo_sistematico = df.iloc[indices]
    return muestreo_sistematico

```

## 1.1 Definición de la función:

```python
def muestreo_sistematico(df, step):

```
**def** es una palabra clave en Python que se utiliza para definir una función. Aquí, estamos definiendo una función llamada muestreo_sistematico.

La función muestreo_sistematico toma dos argumentos:

- df: Es el conjunto de datos sobre el cual se realizará el muestreo.
- step: Es un número entero que indica cada cuántos registros/entradas se tomará una muestra del DataFrame.

## 1.2 Generación de índices sistemáticos:

```python
indices = np.arange(0, len(df), step=step)

```
**np.arange()** es una función de la biblioteca numpy que genera una secuencia de números espaciados uniformemente.

- 0: Es el punto de partida de la secuencia.
- len(df): Determina el punto final de la secuencia. Estamos utilizando la función len() para obtener el número total de filas/entradas en el DataFrame df.
- step=step: Especifica el incremento entre números consecutivos en la secuencia. Por lo tanto, si step es 3, la secuencia generada podría ser [0, 3, 6, 9,...] hasta llegar a un valor inferior a len(df).
El resultado de esta línea es un array de números que indica las posiciones o índices de las filas que se seleccionarán del DataFrame para el muestreo sistemático.

## 1.3 Selección de muestras basada en índices:

```python
muestreo_sistematico = df.iloc[indices]

```
**df.iloc[]** es una función de indexación basada en la posición en pandas. Se utiliza para seleccionar filas/entradas por su posición numérica en el DataFrame.

- **indices** es el array de números que generamos en el paso anterior, que indica qué filas seleccionar del DataFrame df.

El resultado de esta línea es un nuevo DataFrame que contiene sólo las filas especificadas por los índices en el array indices.

## 1.4 Retorno de la muestra:

```python
return muestreo_sistematico

```

