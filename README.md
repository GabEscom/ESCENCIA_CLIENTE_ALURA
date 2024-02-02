# La Escencia del cliente | Challenge | Python | Alura 
<br>
<ul align = center>
<img src=https://github.com/GabEscom/ESCENCIA_CLIENTE_ALURA/assets/147789340/d089f9d7-e791-42b0-a146-35657dc15968>
<br>
<img src="https://img.shields.io/badge/Python-f7e172?style=flat&logo=python" alt="Python Badge">
<img src="https://img.shields.io/badge/Pandas-e00484?style=flat&logo=pandas" alt="Pandas Badge"/>
</ul>

## Descripción 📜
La junta directiva de la cadena de supermercados Universal Food ha observado una estabilización en sus ventas y busca comprender cómo mejorar la relación con sus clientes, entendiendo sus hábitos de compra, para ofrecerles un servicio de mayor calidad. El objetivo es proporcionarles una experiencia de compra más personalizada, rápida y efectiva.

Para abordar este desafio se llevaron acabo las siguientes tareas

### Configuración del entorno 🖥️
Para comenzar, puedes usar cualquier entorno de Python, asegurándote de que sea la versión 3.X. El entorno base es Jupyter Notebook. También necesitarás instalar algunas librerías de Python esenciales para este proyecto, como:
- Pandas
- Numpy
- Matplotlib
- scikit learn

### Obtención de datos 💾
Se realizó la carga de los datos al entorno a partir del proyecto en kaggle 'Media cost prediction on foodmart' (https://www.kaggle.com/datasets/ramjasmaurya/medias-cost-prediction-in-foodmart)

### Exploración de los datos 🔍
Haciendo uso de Matplotlib y Seaborn se generaron diversos gráficos para entender mejor nuestros datos

### Clusterización ⚖

1. El algoritmoutilizado para la clusterización fue KMeans

Validación

2. Se realizó la validación del número de clusters después de instanciar de 3 a 10 clusters con el algoritmo y obtener el puntaje de Silhouette, apara decidir decidir cuál es la mejor configuración para el número de clusters

Restricciones: (El puntaje mínimo de Silhouette esperado debe de ser de 0.50; el de Davies-Bouldin máximo de 0.75; y el de CalinskiHarabasz, el número más alto posible.)

3. Estructura: Se evaluó la estructura de los clusters tomando como referencia una baseline. Para generar la baseline, se generaron números aleatorios con el módulo random de numpy con las mismas dimensiones del dataset para la clusterización asegurandonos de que el df utilizado para clusterización un desempeño muy superior al de random_data.

4. Estabilidad: Se evaluó la estabilidad de los clusters con el número de clusters seleccionado en el paso 2 (5). Para ello, el dataframen estandarizado X_std se dividió en 3 partes iguales. Los puntajes no presentaron una variación mayor a ±5% entre sí.

5. Se instanció el algoritmo de clusterización, con la configuración escogida, y se creo un nuevo atributo en el dataset datos_final llamado 'cluster' para almacenar los labels de los clusters.

### Visualización 📊

6. Finalmente se crearon varios gráficos de dispersión para comparar las variables añadiendo una tercera dimensión con los clusters en el parámetro hue de los gráfico.

### Description ⚙
Legamos a la última parte en la cual se describe el perfil de los clientes de los clusters generados por el modelo y se describe una posible estrategia a utilizar tomando como referencia los resultados obtenidos en pasos anteriores
