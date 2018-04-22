# Hierarchical Risk Parity

El modelo utilizado para solucionar el problema de asset alocation fue el hierarchical Risk Parity, este modelo fue propuesto por Marcos Lopez de Prado (["Building Diversified Portfolios that Outperform Out-of-Sample" (2016)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2708678)). En general el modelo utiliza métodos de inteligencia artificial y grafos para solucionar el problema, el modelo se basa en arboles para reconstruir una estructura herárquica para así restringir el movimiento de la solución del problema al existir choques en los pesos de los activos.

### Estructura del repositorio

La estructura del repositorio es la siguiente. En términos generales se utilizó el modelo de HRP y el benchmark que se utilizó fue el modelo de optimización de portafolios de Markowitz, un modelo de estos optimizando el Sharpe Ratio, el segundo optimiza la volatilidad. La estructura que se acaba de describir está desarrollada en R (en el archivo `Modelo.R`)  y replicada en python para comprobar solides de los algoritmos (en `HRP.ipynb`). En el archivo `records.csv` se encuentra el data frame explicado las configuraciones de los diferentes portafolios generados como también sus métricas más importantes.

## Razones por las cuales se decidió contruir el modelo HRP

Por lo general el modelo de markowitz es el modelo de optimización más reconocido que existe, esto ha llevado a su amplio uso por parte de los analistas financieros, al mismo timepo que ha llevado al olvido de los problemas que posee este modelo. Entre los principales problemas encontramos desde problemas básicos relacionados con los supuestos, cómo la distribución normal y aún más preocupante, el supuesto de datos independientes e identicamente distribuidos, y teniendo encuenta que cada vez es más común que los portafolios posean gran número de acciones, las estructuras intrínsecas en las relaciones de los activos deberían permanecer constantes durante varios periodos de tiempo, lo cual en la vida real no ocurre. Otro problema estructural que presenta el modelo Markowitz es relacionado con las dimensiones, mientras más estas sean, las aproximaciones numéricas hechas por los computadores tienden a aumentar su tamaño que tiene como resultado modificaciones pequeñas pero que resultan signficativas al hallar la inversa de la matriz de covarianza y entiendiendo que este tipo de operaciones son poco estables, estos pequeños cambios resultan en cambios grandes en la inversa, en otras palabras el el portafolio óptimo puede ser solo resultado de aproximaciones numéricas, qué además se suele apoyar en el hecho de que estos tipos de portafolio pierde su optimalidad cuando se tiene en cuenta el tiempo.

los datos por tiempo

## Resultados

## How to run it

## Otros modelos utilizados

## Disclaimers

En realación al código utilizado en los modelos de python es necesario mencionar que el modelo de markowitz está basada en el código del [este](https://github.com/PyDataBlog/Python-for-Data-Science) repositorio mientras que el código utilizado para hrp se base en el modelo original propuesto por Marcos Lopez de Prado

Por el lado de los modelos utilizados en R, estos están basados en el algoritmo origina del siguiente [link](http://economistatlarge.com/portfolio-theory/r-optimized-portfolio) y con respecto al algoritmo utilizado para el modelo de markowitz y graficar la frontera eficiente, el código se basó del algorimo original de [aquí](https://residualmetrics.com/index.php/featured-home/10-finance-markets/39-testing-the-performance-of-hierarchical-risk-parity-for-portfolio-optimisation-using-jse-shares) el cual también está basado directamente en el algorimo original propuesto por Marco Lopez de Prado.
