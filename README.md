# Detección de Noticias Falsas y Sesgo Político

Como sabemos, en las redes sociales cualquier noticia puede volverse viral, sin importar su fuente. Ante esta problemática, se vuelve una necesidad distinguir la veracidad de las noticias, es decir, identificar si son falsas o verdaderas. Además de esto, es crucial comprender qué estructuras contextuales presentan las noticias y qué palabras utilizan para transmitir su mensaje.

Este proyecto utiliza técnicas de machine learning para analizar la veracidad de las noticias. Se emplea aprendizaje supervisado, algoritmos de regresión, agrupamiento y clasificación, así como técnicas de procesamiento de lenguaje natural y el uso de modelos avanzados como BERT (Bidirectional Encoder Representations from Transformers).

## Tecnologías Usadas

Este proyecto fue desarrollado con **Python** y utiliza las siguientes bibliotecas clave:

- **TensorFlow**, **Keras**: Modelos de Machine Learning.
- **Scikit-learn**: Modelos de Machine Learning y evaluación de rendimiento.
- **Pandas**, **NumPy**: Procesamiento de datos.
- **NLTK** Procesamiento de lenguaje natural.
- **Plotly**, **Networkx**, **Matplotlib**, **Seaborn**: Visualización de datos.
- **BeautifulSoup4**, **requests**: Web scraping.

## Instalación

Asegúrate de tener un entorno virtual de Python. Luego, instala las dependencias ejecutando:

```sh
pip install -r requirements.txt
```

### Descarga de Datos

Descarga los archivos **True.csv** y **False.csv** desde el conjunto de datos **[Fake News Detection Datasets](https://onlineacademiccommunity.uvic.ca/isot/2022/11/27/fake-news-detection-datasets/)** del ISOT LAB de la Universidad de Victoria y colócalos en la carpeta `dataset/`. Estos archivos contienen noticias etiquetadas como verdaderas o falsas que serán utilizadas para entrenar y evaluar los modelos.

## Orden recomendado para explorar los notebooks

Para seguir de forma lógica el desarrollo del proyecto, se recomienda revisar los notebooks en el siguiente orden:

### I. Clasificación

1. **[EDA.ipynb](./EDA.ipynb)**  
   *Análisis exploratorio de datos*  
   Se limpian los datos, se analizan las noticias por tema, la distribución de clases y características generales del dataset. 

2. **[NLP.ipynb](./NLP.ipynb)**  
   *Procesamiento de lenguaje natural*  
   Se estudia la frecuencia de palabras, coocurrencias y otras características lingüísticas de las noticias.

3. **[Clasificacion.ipynb](./Clasificacion.ipynb)**  
   *Modelos clásicos de clasificación*  
   Se aplican modelos como Random Forest Classifier y Logistic Regression con métricas como F1-score y vectorizador TF-IDF.

4. **[SVC.ipynb](./SVC.ipynb)**  
   *Support Vector Classifier (SVC)*  
   Se mejora el rendimiento de la máquina de soporte vectorial utilizando GridSearchCV.

5. **[ScrappingNoticias.ipynb](./ScrappingNoticias.ipynb)**  
   *Scraping de nuevas noticias*  
   Se extraen noticias desde la página oficial de la [British Broadcasting Corporation ](https://www.bbc.com/news) para probar el modelo.

6. **[SVC_BBCNews.ipynb](./SVC_BBCNews.ipynb)**  
   *Evaluación en conjunto externo (BBC News)*  
   Se evalúa el modelo SVC con noticias de la BBC.

7. **[BERT.ipynb](./BERT.ipynb)**  
   *Clasificación con BERT (transformers)*  
   Se implementa un modelo BERT para mejorar el rendimiento de clasificación.

## Créditos

- **Zarco Romero José Antonio.** Se encargó del desarrollo de los modelos de clasificación, incluyendo los 7 notebooks correspondientes a esta parte del proyecto.
