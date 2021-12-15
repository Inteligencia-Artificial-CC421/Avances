# Avances

A continuacion se presenta el proyecto en el curso de Inteligencia Artificial CC421, grupo 7:

- Llampi Aliaga, Elias Josue
- Miranda Bailón, Edmundo Manuel  
- Rios Yamamoto, Jose Manuel Yoichi

A continuación se presentará la implementación de la generación de adversarial examples y su aplicación en una red neuronal convolucional pre-entrenada

El objetivo de este trabajo es el poder tomar una imagen que la red neuronal clasifique correctamente, modificarla agregándole ruido a base de sumarle a cada pixel su gradiente multiplicado por un hiperparámetro epsilon el cual dictará que tan fuerte queremos que sea el ruido agregado y volver a evaluar esta nueva imagen en la red para demostrar que ya no es capaz de clasificarla correctamente.

Se usara el método de Fast Gradiente Sign para esta implementación y se presentarán los resultados dados por diferentes valores de epsilon.

##FGSM

FGSM es un método para generar ejemplos adversarios, fue introducido por Goodfellow en el paper Explaining and Harnessing Adversarial Examples. Este método trabaja del siguiente modo:

  1. Toma una imagen de entrada
  2. Realiza una predicción con dicha imagen y el modelo objetivo entrenado.
  3. Calcula la función de pérdida basado en la clasificación correcta o incorrecta de la imagen.
  4. Calcula el signo del gradiente.
  5. Usa el signo del gradiente para construir el ejemplo adversario

Se construye entonces la fórmula:
      x′ = x + e.sign(∇x J(θ, x, y)) 

Donde x es la imagen de entrada, x′ es la imagen modificada, ∇ es el gradiente de la función de costo J respecto a X, con parámetros θ y etiqueta de salida y.
Además, el término e es un número pequeño, que puede ser ajustado a conveniencia, cabe resaltar que mientras más aumente en valor e, la imagen resultante x′ se hará
cada vez más diferente de la imagen original ante los ojos humanos.

El término η, correspondiente a:
  η = sign(∇x J(θ, x, y)) 
es el ruido que se añade a la imagen original x, para generar un ejemplo adversario x

El trabajo de implemento en un modelo entrenado en clasificacion de imagenes de base de datos de tipo MNIST. El archivo jupyter notebook asi como los recursos necesarios puede encontrarlos en la carpeta "Codigo". 

OBSERVACIONES:  Se intento implementar el ataque de tipo FGSM en un modelo de clasificacion de imagenes de tigres, hyenas y cheetas. Sin embargo la implementacion no se culmino para la entrega del proyecto, si desea ver el codigo junto a sus recursos puede encontrarlos en la carpeta "Observaciones"
