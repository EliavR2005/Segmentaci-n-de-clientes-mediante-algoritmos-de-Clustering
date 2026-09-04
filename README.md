# Actividad 3. Segmentación de clientes mediante algoritmos de Clustering

## Algoritmos de aprendizaje automático


---

## Descripción del proyecto

En esta actividad se desarrolla un proceso de **segmentación de clientes mediante algoritmos de aprendizaje no supervisado**, utilizando técnicas de clustering.

El objetivo principal es analizar un conjunto de datos de clientes e identificar grupos con características similares. Para ello se realiza primero una exploración y preparación de los datos, seguida de la aplicación del algoritmo **K-Means**.

Posteriormente, se utilizan diferentes métodos para determinar una cantidad adecuada de clusters, principalmente:

* Método del codo.
* Silhouette Score.

Una vez seleccionada la cantidad de grupos, se analizan las características de cada segmento para identificar perfiles de clientes y proponer estrategias que puedan ser utilizadas por una empresa.

También se utiliza **PCA (Principal Component Analysis)** para representar visualmente los clusters en dos dimensiones y facilitar la interpretación de los resultados.

Finalmente, los resultados de K-Means se comparan con un segundo algoritmo de clustering para analizar las diferencias entre ambos métodos.

---

## Objetivos

### Objetivo general

Realizar una segmentación de clientes mediante algoritmos de clustering para identificar grupos con características similares y analizar su posible aplicación en un contexto empresarial.

### Objetivos específicos

* Explorar y comprender el dataset de clientes.
* Realizar el preprocesamiento necesario para aplicar algoritmos de clustering.
* Escalar las variables utilizadas en el análisis.
* Determinar una cantidad adecuada de clusters mediante el método del codo.
* Evaluar diferentes cantidades de clusters utilizando Silhouette Score.
* Aplicar el algoritmo K-Means.
* Analizar las características promedio de cada segmento.
* Visualizar los clusters mediante PCA.
* Aplicar un segundo algoritmo de clustering.
* Comparar los resultados obtenidos.
* Proponer estrategias de negocio para los segmentos identificados.

---

## Dataset

El proyecto utiliza un dataset de clientes proporcionado para la actividad.

Las variables contienen información relacionada con el comportamiento de los clientes, como:

* Frecuencia de compra.
* Gasto mensual.
* Visitas a la plataforma.
* Uso de descuentos.
* Tiempo desde la última compra.

El archivo utilizado durante el análisis es:

```text
clientes_clustering.csv
```

---

## Metodología

El desarrollo del proyecto se realizó mediante las siguientes etapas:

### 1. Exploración de los datos

Se realizó una revisión inicial del dataset para conocer:

* Número de registros.
* Número de variables.
* Tipos de datos.
* Valores faltantes.
* Estadísticas descriptivas.
* Distribución de las variables.

### 2. Preprocesamiento

Se prepararon los datos para aplicar los algoritmos de clustering.

Una parte importante del proceso fue el **escalamiento de las variables**, debido a que K-Means utiliza distancias para determinar qué registros pertenecen a cada grupo.

Si una variable tiene valores mucho mayores que otra, podría tener una influencia excesiva sobre el resultado. Por esta razón, las variables fueron escaladas antes de aplicar el algoritmo.

### 3. Determinación del número de clusters

Se utilizaron dos métodos para analizar diferentes cantidades de grupos:

#### Método del codo

Se calcularon los valores de inercia para diferentes cantidades de clusters y se generó una gráfica para identificar el punto en el que agregar más grupos deja de producir una mejora significativa.

#### Silhouette Score

También se calculó el Silhouette Score para diferentes valores de K.

Esta métrica permite evaluar qué tan bien separados se encuentran los grupos. Un valor mayor indica, en general, una mejor separación entre los clusters.

### 4. K-Means

Después de analizar los resultados anteriores, se seleccionó una cantidad de clusters y se aplicó el algoritmo K-Means al conjunto de datos previamente escalado.

Posteriormente se analizaron:

* Cantidad de clientes por cluster.
* Promedios de las variables.
* Diferencias entre segmentos.
* Características principales de cada grupo.

### 5. PCA

Se utilizó **PCA (Principal Component Analysis)** para reducir las dimensiones de los datos y representar los clusters utilizando dos componentes principales:

* PC1.
* PC2.

Esta visualización permite observar de manera gráfica la distribución y separación de los grupos encontrados.

### 6. Comparación con otro algoritmo

Finalmente, se aplicó un segundo algoritmo de clustering para comparar sus resultados con K-Means.

Se analizaron las diferencias en:

* Número de grupos encontrados.
* Distribución de los clientes.
* Separación de los grupos.
* Interpretación de los segmentos.

---

## Tecnologías utilizadas

El proyecto fue desarrollado utilizando:

* **Python**
* **Google Colab**
* **Jupyter Notebook**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**

Las principales herramientas de Scikit-learn utilizadas fueron:

* `KMeans`
* `StandardScaler`
* `silhouette_score`
* `PCA`
* Algoritmo adicional de clustering utilizado en la comparación.

---

## Estructura del proyecto

```text
Actividad-3-Clustering/
│
├── clientes_clustering.csv
├── Actividad_3_Clustering.ipynb
├── README.md
└── reporte/
    └── Reporte_Actividad_3.pdf
```

---

## Resultados

El análisis permite identificar diferentes segmentos de clientes de acuerdo con sus características y comportamiento dentro del dataset.

Los resultados finales de los clusters, incluyendo la cantidad de clientes, características promedio y nombres asignados a cada segmento, se encuentran documentados en el reporte de la actividad y en el Notebook.

La visualización mediante PCA permite observar gráficamente la distribución de los segmentos encontrados.

---

## Aplicación al negocio

La segmentación de clientes puede ser utilizada por una empresa para desarrollar estrategias específicas para cada grupo.

Por ejemplo, dependiendo de las características encontradas, pueden diseñarse estrategias relacionadas con:

* Promociones personalizadas.
* Programas de fidelización.
* Descuentos.
* Recomendaciones de productos.
* Campañas de reactivación.
* Estrategias para aumentar la frecuencia de compra.

De esta manera, en lugar de aplicar una misma estrategia para todos los clientes, la empresa puede adaptar sus acciones de acuerdo con las características de cada segmento.

---

## Notebook

El desarrollo completo del análisis se encuentra en el siguiente archivo:

**`Actividad_3_Clustering.ipynb`**

El Notebook contiene el código ejecutado, las gráficas generadas y los resultados obtenidos durante cada etapa del proceso.

---

## Autor

**Eliab Reyes Olvera**

Proyecto realizado como parte de la actividad **Segmentación de clientes mediante algoritmos de Clustering** de la materia **Algoritmos de aprendizaje automático**.
