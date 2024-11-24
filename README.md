# Sistema de Recomendación de Anime
## Estructura del proyecto
- analisis_files: Notebooks de python donde analizamos los datos y vimos con cuales datos estabamos trabajando.
- data_lab: Los archivos de modelos de prueba
- model_files: Los notebooks con los modelos finales
- process: Los archivos de datos con el preprocesamiento hecho.
- processing_files: Los archivos que hicieron el preprocesamiento. (Bastante del preprosesamiento se hacia en los modelos finales)
- refined: Los datos y modelos que nos quedaron después de hacer el procesamiento
- testing_files: Unos archivos para asegurar que los resultados fueran correctos.
## Correr el modelos finales
### Descargar datos
Los datos que usamos son de Kaggle usamos este [dataset](https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset).
### Análisis de datos
Para correr el análisis se puede usar cualquier programa que corra Jupyter notebook en la parte de arriba se instalan las dependencias de los notebooks.
### Crear Arquitectura
1. Crear una carpeta en s3. [Tutorial](https://scribehow.com/shared/Create_an_S3_Bucket_and_Upload_Files__IpMbFfdaSzuxviU2n_Ec8Q)
2. Crear un cluster EMR. [Tutorial]()
### Entrenar Modelos
Correr los archivos en cluster EMR. [Tutorial]()
