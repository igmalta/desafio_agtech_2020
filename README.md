
[Meta: Data - Competencia en ciencia de Datos - Desafíos AgTech 2020](https://metadata.fundacionsadosky.org.ar/competition/22/)

# Clasificación de cultivos utilizando imágenes satelitales

> **4° Puesto** | Puntaje Público: **0.62821** - Puntaje Privado: **0.52524** (Balanced accuracy)

## Objetivo del concurso
Construir un método de aprendizaje supervisado que mediante imágenes satelitales y la verdad de campo de cosechas previas pueda clasificar cultivos para distintos puntos geográficos del departamento de General López, Santa Fe.

## Solución
Se propone un modelo de clasificación de cultivos con imágenes obtenidas de los satélites Landsat 8, Sentinel 1 y Sentinel 2 a través de la API Google Earth Engine. 

![Zona de Interés]("data/img/zona_estudio.PNG")

El modelo consiste en un algoritmo de Gradient Boosting, el framework Lightgbm. Se construye un conjunto de datos estructurado usando las bandas de las imágenes descargadas de la API GEE como variables ("columnas") y adicionalmente se realiza "feature engineering". 

## Archivos
- Informe del trabajo: **informe_desafio_agtech_2020.ipynb**
- Datos de entrenamiento de entrada del modelo propuesto: **data/train_model_lgbm_02_141220.csv**
- Datos de evaluación utilizados para las predicciones: **data/train_model_lgbm_02_141220.csv**
- Etiquetas de los cultivos: **data/etiquetas.csv**
- Perímetro del área de interés: **data/aoi/Gral Lopez.shp**
- Modelo entrenado final: **data/output/lgbm_classifier_02_141220.pkl**
- Datos de la solución (categorías reales): **data_test_solucion.csv**

## Ejecución Local
Se recomienda instalar un entorno virtual, luego:

```
pip install -r requirements.txt 
```

*Guía de instalación de Lightgbm:* https://lightgbm.readthedocs.io/en/latest/Installation-Guide.html

Finalmente abrir `../informe_desafio_agtech_2020.ipynb`

