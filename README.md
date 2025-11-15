# Análisis de datos de Monefy

Este notebook realiza un análisis exploratorio de un archivo CSV exportado desde la aplicación Monefy. El objetivo es transformar los datos originales en información útil para revisar gastos, ingresos y patrones financieros del periodo analizado.

## Qué hace este análisis

1. Carga del archivo CSV  
   Se importa el dataset exportado desde Monefy y se revisa su estructura básica para asegurar que los datos vienen correctamente formateados.

2. Limpieza de cantidades  
   Los valores monetarios de Monefy vienen con diferentes formatos.  
   En el notebook se convierten estas cantidades a valores numéricos utilizables para cálculos.

3. Conversión y extracción de fechas  
   La fecha se transforma a formato datetime y se crean columnas como año, mes, día y día de la semana.  
   Esto permite organizar y analizar los movimientos por periodos.

4. Clasificación de movimientos  
   Cada registro se identifica como gasto, ingreso, transferencia o saldo inicial.  
   Esto permite separar los gastos reales de movimientos internos entre cuentas.

5. Resumen general del periodo  
   El notebook calcula:
   - total de gastos reales  
   - total de ingresos reales  
   - neto del periodo  
   - gasto medio diario  
   También muestra los días con mayor o menor movimiento económico.

6. Análisis por categorías y cuentas  
   Se determina en qué categorías se gasta más y desde qué cuentas salen los movimientos principales.

7. Flujo económico diario  
   Se genera una serie temporal que muestra el movimiento neto de cada día del periodo.  
   Esto permite detectar picos y tendencias.

8. Funciones reutilizables  
   El notebook incluye funciones para reutilizar este mismo análisis con cualquier CSV futuro de Monefy, cambiando únicamente la ruta del archivo.

## Objetivo general

Convertir los datos de Monefy en una visión clara del comportamiento financiero, permitiendo detectar hábitos de gasto, tendencias diarias y patrones entre cuentas y categorías de manera sencilla y automatizada.