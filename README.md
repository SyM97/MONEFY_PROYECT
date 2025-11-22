# Análisis de datos de Monefy

Este notebook realiza un análisis exploratorio de un archivo CSV exportado desde la aplicación Monefy. El objetivo es transformar los datos originales en información útil para revisar gastos, ingresos y patrones financieros del periodo analizado.

## Qué hace este análisis

1. Carga del archivo CSV  
   Se importa el dataset exportado desde Monefy y se revisa su estructura básica para asegurar que los datos vienen correctamente formateados.

2. Limpieza de cantidades  
   Los valores monetarios de Monefy pueden venir con diferentes formatos (puntos, comas, varios separadores, etc.).  
   En el notebook se convierten estas cantidades a valores numéricos utilizables para cálculos, corrigiendo casos como "3.952.17" → 3952.17.

3. Conversión de fechas  
   La fecha se transforma a formato datetime con el día primero (día/mes/año).  
   Esto permite agrupar y analizar los movimientos por día y por periodo de tiempo.

4. Clasificación de movimientos  
   Cada registro se clasifica automáticamente como:
   - saldo inicial  
   - transferencia  
   - gasto  
   - ingreso  
   De esta forma se separan los gastos reales de los movimientos internos entre cuentas y de los saldos iniciales.

5. Creación de un dataset de movimientos reales  
   A partir del dataset original se genera un dataframe filtrado sin saldos iniciales ni transferencias.  
   En este dataframe se añaden columnas auxiliares para identificar claramente importes de gasto, ingresos y sus valores absolutos.

6. Resumen general del periodo  
   El notebook calcula, a partir de los movimientos reales:
   - total de gastos  
   - total de ingresos  
   - neto del periodo  
   - neto diario (ingresos − gastos por día)

7. Análisis por categorías y cuentas  
   Se agrupan los datos para obtener:
   - gastos totales por categoría y número de movimientos  
   - ingresos por categoría (si los hay)  
   - gastos totales por cuenta  
   También se calcula el porcentaje del gasto total que representa cada categoría.

8. Flujo económico diario y tablas dinámicas  
   Se genera una serie temporal con el neto diario y una tabla tipo pivot con el neto por día y por cuenta, lo que permite detectar picos, días más movidos y qué cuentas se usan más.

9. Visualizaciones  
   El notebook incluye varias gráficas para una lectura más clara:
   - gráfico de barras de gastos por categoría con degradado de color según el nivel de gasto  
   - gráfico de porcentaje del gasto por categoría  
   - líneas de neto diario y neto acumulado en el tiempo  
   - mapa de calor del neto diario por cuenta  

10. Funciones reutilizables  
    El notebook organiza la lógica en funciones, de forma que se puede repetir el mismo análisis con cualquier CSV futuro exportado desde Monefy cambiando únicamente la ruta del archivo.

## Objetivo general

Convertir los datos de Monefy en una visión clara del comportamiento financiero, permitiendo detectar hábitos de gasto, tendencias diarias y patrones entre cuentas y categorías de manera sencilla, visual y automatizada.
