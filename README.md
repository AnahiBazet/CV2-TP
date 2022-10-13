# CV2-TP
Este repositorio contiene el trabajo práctico de la materia Visión por Computadora II de la Carrera de Especialización en Inteligencia Artificial (CEIA) de la FIUBA realizado por Lionel Gutiérrez y Anahi Bazet.

## Objetivo

Dada una imagen de una habitación de una vivienda se determina si se trata de un baño, un dormitorio, un comedor, una cocina o un living. Es un problema de clasificación multi-clase de 5 clases.

## Parte I: modelos con transfer learning

Para poder resolverlo, se aplican diferentes tipos de redes neuronales de clasificación (VGG19, ResNet50, Inception V3 y AlexNet) con trasfer-learning (feature extraction) y data augmentation: rotación, color jitter (matiz, contraste y brillo) y desenfoque gaussiano. Luego, se comparan resultados y se extraen conclusiones.

Por otro lado, para el caso particular de AlexNet, se evalúa la performance de la red combinando las transformaciones de data augmentation aplicadas (rotación, color jitter y desenfoque gaussiano) hasta que no queda ninguna. También se aplica una estrategia de escala de grises para comparar con la de color jitter. Por último, se utiliza AutoAugment. En este caso, también se comparan resultados y se extraen conclusiones.

Otra cuestión que se analiza, es lo que sucede si no se aplica transfer learning a Alexnet, es decir, si se entrenan todos sus pesos. En este caso se aplica con y sin data augmentation, lo que podemos encontrar en la otra notebook "TP final CV2- 5Cohorte CEIA- Habitaciones-Modelo-sin-transfer-learning". También se comparan esos resultados, con los obtenidos en esta notebook para AlexNet con transfer learning (con y sin data augmentation).

Colab: [Con transfer learning](https://github.com/AnahiBazet/CV2-TP/blob/main/TP_final_CV2-5Cohorte_CEIA-%20Habitaciones.ipynb)

## Parte II: modelos sin transfer learning

Aquí se busca entrenar el modelo AlexNet si aplicar transfer learning, es decir, entrenando todos sus pesos. Precisamente, se ejecutan dos variantes:

* La primera, utiliza todos los tipos de data augmentation elegidos en la notebook principal.
* La segunda, no aplica data augmentation.

Por último, se extraen conclusiones comparando con el modelo de Alexnet en donde se aplicó transfer learning, tanto cuando posee data augmentation, como cuando no se utiliza.

Colab: [Sin transfer learning](https://github.com/AnahiBazet/CV2-TP/blob/main/TP_final_CV2-5Cohorte_CEIA-%20Habitaciones-Modelo-sin-transfer-learning.ipynb)

## Presentación

Se expone el trabajo práctico completo.

PDF: [Presentación](https://github.com/AnahiBazet/CV2-TP/blob/main/Presentaci%C3%B3n/TP%20Visi%C3%B3n%20por%20Computadora%20II%20-%20Clasificaci%C3%B3n%20de%20habitaciones.pdf)
