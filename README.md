# Deteccion de genero
El modelo keras se crea al entrenar SmallerVGGNet desde cero en alrededor de 2200 imágenes faciales (~ 1100 para cada clase). La región de la cara se recorta aplicando face detectionusando cvliblas imágenes recopiladas de Google Images. Obtuvo alrededor del 96% de precisión de entrenamiento y ~ 90% de precisión de validación. (20% del conjunto de datos se usa para la validación)
Actualización:
Verifique la funcionalidad de detección de género implementada en cvlib a la que se puede acceder a través de una sola llamada de función detect_gender().

## Paquetes de Python
numpy
opencv-python
Tensorflow
keras
peticiones
barra de progreso
cvlib
Instale los paquetes requeridos ejecutando el siguiente comando.

$ pip install -r requirements.txt

Nota: Python 2.x no es compatible

Asegúrese de que pipesté vinculado a Python 3.x ( pip -Vmostrará esta información).

Si pipestá vinculado a Python 2.7. Usar en su pip3lugar. pip3se puede instalar usando el comandosudo apt-get install python3-pip

Se recomienda utilizar el entorno virtual de Python .

# Uso
## entrada de imagen
$ python detect_gender.py -i <input_image>

# cámara web
$ python detect_gender_webcam.py

Cuando ejecuta el script por primera vez, descargará el modelo previamente entrenado desde este enlace y lo colocará en el pre-traineddirectorio de la ruta actual.

(Si el pythoncomando invoca Python 2.7 predeterminado, use python3en su lugar)

## Salida de muestra:


Formación
Puede descargar el conjunto de datos que reuní de Google Images desde este enlace y capacitar a la red desde cero por su cuenta si está interesado. Puede agregar más imágenes y jugar con los hiperparámetros para experimentar diferentes ideas.

## Paquetes adicionales
scikit-learn
matplotlib
Instálelos escribiendo pip install scikit-learn matplotlib

## Uso
Comience el entrenamiento ejecutando el comando

$ python train.py -d <path-to-dataset>

(es decir, $ python train.py -d ~ / Downloads / gender_dataset_face /

Dependiendo de la configuración de hardware de su sistema, el tiempo de ejecución variará. En la CPU, el entrenamiento será lento. Después del entrenamiento, el archivo del modelo se guardará en la ruta actual como gender_detection.model.

Si tiene una GPU Nvidia, puede instalar el tensorflow-gpupaquete. Hará que las cosas funcionen mucho más rápido.
