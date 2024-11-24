# Sistema de Recomendación de Anime
## Estructura del proyecto
- analisis_files: Notebooks de python donde analizamos los datos y vimos con cuales datos estabamos trabajando.
- data_lab: Los archivos de modelos de prueba
- model_files: Los notebooks con procesamiento y modelos finales
- sample_files: Los archivos de datos con el preprocesamiento hecho.
- sample_test: Los archivos que hicieron el preprocesamiento. (Bastante del preprosesamiento se hacia en los modelos finales)
- refined: Los datos y modelos que nos quedaron después de hacer el procesamiento. Esto es lo modelos en si como los guarda pyspark. También, tiene los resultados como los vectores tfidf, y las recommendaciones del colaborative filtering.
Ejemplo:
```python
from pyspark.ml.recommendation import ALSModel

model = ALSModel.load("refined/anime_recommendations_als_model")
```
```python
from pyspark.ml import PipelineModel

pipeline_model = PipelineModel.load("refined/tfidf_pipeline_model")
```
- testing_files: Unos archivos para asegurar que los resultados fueran correctos. Revisar que los ids si existieran y buscar las recommendaciones.
## Correr Código
### Descargar datos
Los datos que usamos son de Kaggle usamos este [dataset](https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset).
### Análisis de datos
Para correr el análisis se puede usar cualquier programa que corra Jupyter notebook en la parte de arriba se instalan las dependencias de los notebooks.
### Crear Arquitectura
1. Crear una carpeta en s3. [Tutorial](https://scribehow.com/shared/Create_an_S3_Bucket_and_Upload_Files__IpMbFfdaSzuxviU2n_Ec8Q)
2. Crear un cluster EMR. [Tutorial](https://scribehow.com/shared/Create_an_Amazon_EMR_Cluster_with_Custom_Security_Rules__23RSSB9SSK65adYhDhfVsg)
### Entrenar Modelos
Correr los archivos en cluster EMR. [Tutorial](https://scribehow.com/shared/Uploading_and_Running_a_Jupyter_Notebook_on_EMR__zc2LkutZSKWVO7PlnPY4dQ)
