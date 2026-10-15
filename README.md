# Proyecto 2: Clasificación de tejidos en imágenes de cáncer colorrectal

Proyecto de visión artificial. Universidad de Medellín, Ingeniería de Sistemas.

**Autor:** Sebastián Quintero Granada

## Descripción

Clasificamos imágenes de tejido de cáncer colorrectal vistas al microscopio en 8 tipos de tejido: epitelio tumoral, estroma simple, estroma complejo, células inmunes, detritos y moco, glándulas mucosas, tejido adiposo y fondo.

La base es [`colorectal_histology`](https://www.tensorflow.org/datasets/catalog/colorectal_histology) de TensorFlow Datasets: 5.000 imágenes RGB de 150 × 150 píxeles. El notebook la descarga directamente con `tfds.load`, por eso no está en el repositorio.

Aplicamos fine tuning sobre VGG16 y ResNet50 preentrenadas en ImageNet. Con una malla de hiperparámetros (arquitectura × batch size × learning rate) escogemos el mejor modelo, y al final lo evaluamos en un conjunto de prueba.

## Cómo ejecutarlo

Abrir `proyecto2_vision_artificial.ipynb` en Google Colab, activar la GPU (Entorno de ejecución → Cambiar tipo de entorno → GPU T4) y ejecutar todas las celdas.
