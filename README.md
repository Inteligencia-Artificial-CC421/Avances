# Avances

A continuacion se presenta el proyecto en el curso de Inteligencia Artificial CC421, grupo 7:

- Llampi Aliaga, Elias Josue
- Miranda Bailón, Edmundo Manuel  
- Rios Yamamoto, Jose Manuel Yoichi

A continuación se presentará la implementación de la generación de adversarial examples y su aplicación en una red neuronal convolucional pre-entrenada

El objetivo de este código es el poder tomar una imagen que la red neuronal clasifique correctamente, modificarla agregándole ruido a base de sumarle a cada pixel su gradiente multiplicado por un hiperparámetro epsilon el cual dictará que tan fuerte queremos que sea el ruido agregado y volver a evaluar esta nueva imagen en la red para demostrar que ya no es capaz de clasificarla correctamente

Se usara el método de Fast Gradiente Sign para esta implementación y se presentarán los resultados dados por diferentes valores de epsilon.
