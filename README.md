# Análisis de Fricción Logística y Percepción del Cliente en E-Commerce (Olist Brasil)

Proyecto enfocado en identificar qué variables operativas, geográficas y de producto detonan las calificaciones negativas (clientes detractores de 1 y 2 estrellas) en el marketplace brasileño Olist entre 2016 y 2018.

## Contenido del Repositorio
* [Entrega_1_de_DataScience_II.ipynb](./Entrega_1_de_DataScience_II.ipynb): Cuaderno de Google Colab con la integración de tablas relacionales, consulta a API cambiaria, limpieza de datos, análisis exploratorio visual y conclusiones.
* [Entrega 1 DataScience II.pdf](./Entrega%201%20DataScience%20II.pdf): Presentación con el contexto de negocio, hipótesis, hallazgos clave, recomendaciones y proyección hacia el modelado predictivo.

## Metodología y Limpieza de Datos
Para construir la base analítica se integraron cinco tablas relacionales del dataset público de Olist en Kaggle (órdenes, artículos, productos, clientes y reseñas) junto con una consulta a una API externa para convertir precios y fletes de reales brasileños (BRL) a dólares (USD). Tras filtrar únicamente pedidos efectivamente entregados (`delivered`), corregir inconsistencias temporales, imputar dimensiones físicas faltantes mediante la mediana y recortar tiempos atípicos superiores al percentil 99,5 (53,2 días), se consolidó una muestra limpia de 98.997 transacciones, con una tasa base del **13,59% de clientes detractores**.

## Principales Hallazgos
El análisis demuestra que el cumplimiento de la fecha prometida es el factor determinante de la satisfacción poscompra lo que quiere decir que recibir un paquete con retraso multiplica por cinco la proporción de detractores, pasando del 10,1% en entregas puntuales al 53,1% en entregas tardías. En contraste, cuando el costo de envío supera el 33% del valor del producto, la detracción apenas asciende al 14,3%, lo que confirma que el comprador tolera pagar flete siempre que se respete el plazo acordado.

En el plano territorial, más del 86% de los despachos nacen en el eje sureste-sur conformado por São Paulo (71,32%), Minas Gerais (7,84%) y Paraná (7,70%). Esta cercanía mantiene tasas de demora bajas en esa región (entre 4,7% y 5,5%), mientras que destinos más alejados como Bahía (12,6%), Río de Janeiro (11,9%) y Espírito Santo (11,3%) sufren más del doble de incumplimiento logístico.

A esta brecha geográfica se suma la fricción física y de catálogo, los productos pesados (mayores a 5 kg) promedian 13,7 días en tránsito frente a 11,7 días en paquetes livianos (menores a 1 kg), lo que explica que categorías voluminosas o delicadas como Cama Mesa Banho (17,3%) y Moveis Decoracao (15,9%) lideren la insatisfacción. Finalmente, aunque se registraron picos puntuales de retraso en noviembre de 2017 y marzo de 2018 (20%), en otros meses con alto volumen de compras las demoras disminuyeron, indicando que los retrasos responden más a distancias de ruta, peso de carga y promesas poco realistas que únicamente al volumen mensual.
