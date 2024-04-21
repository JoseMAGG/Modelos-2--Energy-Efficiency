# Modelos 2 - Energy Efficiency
Este repositorio contiene los notebooks y bases de datos utilizados para el proyecto de aula de la materia Modelos y Simulación de Sistemas 2, de la Ingeniería de Sistemas, en la Universidad de Antioquia.

## Files
La carpeta files contiene las bases de datos utilizadas.
- **Energy-Efficiency** contiene la base de datos original en formato xlsx, la cuál fue simulada por Athanasios Tsanas y Angeliki Xifara y publicada en el repositorio de machine learning UCI (https://doi.org/10.24432/C51307).
- **BD_10_Reg(Normalizado)** contiene las variables de entrada normalizadas y la variable de salida escogida: Heating Load. Para este proyecto se requería escoger una única variable de salida para el problema de regresión.

## EDA
El análisis exploratorio de los datos (EDA) es un notebook, trabajado en Google Colab, donde se carga la base de datos original para revisar los tipos de datos, relación entre variables y datos faltantes en las variables de entrada y salida. Aquí también se selecciona la variable de salida, se normalizan los datos no categóricos y se exporta una nueva base de datos en formato csv para su utilización en las siguientes fases.

## Modelos
En este notebook se hace uso de la base de datos normalizada para entrenar 4 diferentes modelos de regresión. Los datos se dividen en 80% para entrenamiento y 20% para validación. Los modelos utilizados son *Multiple Linear Regressor*, *K Neighbors Regressor*, *Polynomial Regression* y *Decision Trees*, todos del repositorio *sklearn*. Para cada uno de estos modelos se realiza el entrenamiento con los mismos datos, de igual forma, se generan las predicciones con los mismos datos de validación. Se grafica la diferencia entre los valores reales y los valores predichos para cada modelo.
Al final del notebook, se calculan las métricas de media cuadrada del error (*MSE*) y *R squared score* tanto en el entrenamiento como en la validación, con el objetivo de realizar una tabla comparativa para todos los modelos y seleccionar el mejor de estos.
