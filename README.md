# Car Damage Project

### Laura Gutiérrez y Natalia Mirón
### Abril 2022

## La idea
Este proyecto es el trabajo de IMAGEN del Máster de Big Data y Analítica avanzada para la asignatura de Análisis de Datos no Estructurados.

¿Alguna vez te has planteado que una máquina determine si un coche necesita ser reparado o ha tenido un accidente?

El proyecto tiene como idea base ser un clasificador de coches con daños, pudiéndose utilizar para aseguradoras.
Se usa una base de datos con 1840 imágenes de coches enteros y dañados en el entrenamiento.

Hay dos clasificadores:
1. **Clasificador de Vehículos**: Responde a la pregunta de ¿es un coche o no? - Scripts que empiezan por "01"
3. **Clasificador de Vehículos Dañados**: Responde a la pregunta de ¿el coche tiene daños o no? - Scripts que empiezan por "02"

## Nuestra Propuesta
Se separa en 5 scripts que deben de ejecutarse uno tras otro.

  1. **01_CarOrNot.ipynb**: Es un clasificador de vehículos. Al insertar una imagen, el clasificador predice si en la imagen se detecta que hay un vehículo o no. Si detecta que hay un vehículo se puede pasar a la segunda clasificación.
  2. **02.0_DamagedOrNot_Analysis.ipynb**: Es el análisis exploratorio de la base de datos usada y la primera iteración de nuestro clasificador de Vehículos Dañados.
  3. **02.1_DamagedOrNot.ipynb**: La última iteración de nuestro clasificador de Vehículos Dañados. Carga el modelo preentrenado vgg16 sin su última capa, lo entrena y lo guarda.
  4. **02.2_DamagedOrNot_Logistic.ipynb**: Continúa con la ejecución del script **02.1_DamagedOrNot.ipynb**, y se ejecuta un modelo de regresión logística para medir la precisión de nuestro modelo.
  5. **02.1_DamagedOrNot_Prediction.ipynb**: Predice si hay daños en nuevas imágenes que se inserten cargando el modelo entrenado en los scripts anteriores. 


A su vez, hay 5 carpetas donde guardamos resultados y modelos:
*	**car_damage_check**: se guarda todo lo referente al modelo bueno que es el pre-entrenado
•	**data**: en esta carpeta está el cat_counter (se utiliza en el script 01)
•	**images**: en esta carpeta está el modelo vgg que se utiliza en el primer script y otra carpeta con las imágenes de los ejemplos que vamos poniendo
•	**models**: aquí guardamos todos nuestros modelos con extensión .h5
•	**training & validation**: estos son los conjuntos de datos que utilizamos para entrenar y validar (fotos de los coches normales y dañados)


¡Esperamos que os haya resultado interesante!
