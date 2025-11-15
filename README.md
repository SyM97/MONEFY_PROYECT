# Análisis de gastos desde datos exportados de Monefy

Este proyecto toma un archivo CSV exportado desde la aplicación Monefy y lo transforma en un informe claro y útil sobre los gastos personales. El objetivo es convertir los datos brutos en información ordenada, comprensible y lista para tomar decisiones.

## Proceso del análisis

1. Carga del archivo  
   Se importa el CSV de Monefy y se visualizan las primeras filas para verificar su estructura.

2. Limpieza de datos  
   Se convierten las cantidades de dinero a formato numérico y se normalizan las fechas.  
   Esto permite realizar cálculos correctos y trabajar con fechas como valores reales.

3. Identificación del tipo de movimiento  
   Cada registro del archivo se clasifica como gasto, ingreso, transferencia o saldo inicial.  
   Esto permite separar el dinero realmente gastado de los movimientos internos entre cuentas.

4. Resumen general  
   Se calcula el total de ingresos, gastos reales, neto del periodo y medias diarias.  
   Con ello se obtiene una visión rápida de la salud financiera del periodo analizado.

5. Análisis por categorías y cuentas  
   Se identifican las categorías donde más se gasta y las cuentas desde las que salen los gastos.  
   Esto permite detectar hábitos, áreas de mayor gasto y patrones de uso de cada cuenta.

6. Flujo diario  
   Se genera una serie temporal del gasto/ingreso de cada día del periodo.  
   Esto permite ver picos, tendencias o días con movimiento inusual.

## Objetivo final

El análisis permite convertir los datos exportados desde Monefy en:
- información clara,
- métricas útiles,
- gráficos interpretables,
- y un resumen general fácil de revisar.

Además, incluye funciones reutilizables para analizar cualquier futuro archivo CSV de Monefy cambiando solo la ruta del archivo.