Uvas
================
Benjamin Lira
3/27/2020

Introducción
============

En este documento reportaré el procedimiento seguido para crear un algoritmo que prediga la fecha de la cosecha tomando en cuenta la variedad, carga y fecha de aplicación de cianamida, tomando en cuenta datos de clima histórico.

### Descripción del algoritmo objetivo

Para poder cumplir con el objetivo de predecir la fecha de cosecha en base a variedad, carga, clima y fecha de aplicación de cianamida tenemos que hacer lo siguiente.

1.  Calcular la cantidad de horas/calor sobre 16 grados (solo los positivos) para la data histórica. Sumar el total por el día. Promediar las fechas iguales (ignorando el año).

2.  Predecir la cantidad de horas/sol necesarias (del año específico que tenemos la data, no del histórico), la carga y la variedad.

3.  En base a ese modelo, podemos predecir la cantidad de horas que son necesarias para la madurez dependiendo de la carga y variedad

4.  Buscar en la data histórica cuantos días son necesarios desde la aplicación de la cianamida para lograr esa cantidad predicha de horas sol

5.  Sumar esa cantidad de días a la aplicación de la cianamida para tener la fecha estimada de cosecha

Procedimiento
=============

### Revisión de los datos iniciales

La calidad de un modelo predictivo, dependerá de que los insumos de los que se alimenta sean precisos. Vamos a revisar que no hayan cosas extrañas en los datos de la fuente para asegurarnos de la calidad de los datos.

### Cargar las bases de datos

Comenzamos por cargar los datos de Clima (`Clima`) y de maduración de uvas (`Uvas`). En ambos casos estamos seleccionando únicamente las variables que vamos a emplear. En cuanto a la temperatura, estamos usando la variable `Temperatura Exterior` como indicador, y dejando de lado la máxima y la mínima que también están disponibles en la base de datos.

### Definir el indice de calor más apropiado

### Calcular el indice de calor en el clima histórico

### Predecir la cantidad de horas calor necesarias para la madurez (año 2019)

### Calcular cantidad de días después de la aplicación de cianamida se lograrán las horas calor necesarias

### Usar esta información para estimar la fecha de cosecha.
