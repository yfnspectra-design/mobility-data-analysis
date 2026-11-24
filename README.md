# Movilidad urbana y productividad económica en Latinoamérica (2024)


## Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón para abrir el proyecto en Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yfnspectra-design/mobility-data-analysis/blob/main/Sprint_5_Analisis_de_Movilidad.ipynb)

Proyecto de análisis exploratorio de datos (Sprint 5). Se estudia la relación entre los indicadores de movilidad urbana y el PIB per cápita de ciudades latinoamericanas para identificar posibles prioridades de inversión en infraestructura de transporte.

## Fuentes de datos

- **TomTom Traffic Index** (`tomtom_traffic.csv`): 1,004,464 registros originales de tráfico, con indicadores de congestión, retrasos y tiempos de viaje.
- **OECD Cities** (`oecd_city_economy.csv`): 30 registros originales de indicadores económicos, demográficos y ambientales.

El análisis de tráfico de 2024 comprende 387 ciudades. La unión de las dos fuentes permite comparar 15 ciudades de siete países latinoamericanos: Argentina, Brasil, Chile, Colombia, México, Perú y Uruguay.

## Metodología

1. Exploración de tipos de datos y valores ausentes.
2. Estandarización de columnas y conversión de fechas y formatos numéricos.
3. Filtrado de registros correspondientes a 2024.
4. Agregación de indicadores de tráfico por ciudad, país y año.
5. Integración mediante una unión interna por ciudad y año.
6. Visualización mediante boxplot, histograma y gráfico de barras.
7. Exportación de resultados y elaboración de un resumen ejecutivo.

## Resultados principales

| Indicador | Resultado |
|---|---:|
| Retraso agregado promedio por registro en Ciudad de México | 2,833.06 min |
| Retraso agregado promedio en las 15 ciudades de la muestra integrada | 629.52 min |
| Retraso agregado promedio en Bogotá | 1,141.55 min |
| PIB per cápita en Bogotá | 11,442 USD |
| Retraso agregado promedio en Buenos Aires | 571.09 min |
| PIB per cápita en Buenos Aires | 18,117 USD |

No se observa una relación visual simple y uniforme entre congestión vehicular y PIB per cápita. Bogotá podría ser una ciudad prioritaria para evaluar inversiones de transporte por combinar retrasos elevados con un PIB per cápita relativamente bajo dentro de la muestra. Ciudad de México también merece atención por sus niveles de congestión.

Estos resultados son exploratorios: el PIB per cápita se utiliza como indicador económico aproximado y los retrasos agregados de la red no equivalen a tiempos de espera por persona. No se establece causalidad ni significancia estadística. Se recomienda ampliar el análisis a varios años e incorporar datos de población, demanda de movilidad y transporte público.

## Herramientas

Python, Pandas, NumPy, Matplotlib, Seaborn y Jupyter Notebook.

## Reproducir el análisis

1. Descarga o clona este repositorio.
2. Instala las dependencias:

   ```bash
   pip install pandas numpy matplotlib seaborn notebook
   ```

3. Obtén los dos CSV originales del proyecto y colócalos en una carpeta `datasets/` junto al notebook (también se admite colocarlos directamente junto al notebook). Los archivos fuente no se incluyen en esta entrega; revisa sus condiciones de uso antes de compartirlos públicamente.
4. Abre `Sprint_5_Analisis_de_Movilidad.ipynb` en Jupyter y ejecuta todas las celdas en orden.
5. El notebook genera `ladb_mobility_economy_2024_clean.csv` al finalizar.

El notebook incluye las salidas y gráficas conservadas del análisis original, por lo que es posible consultarlas sin ejecutar el código.

## Estructura

```text
mobility-data-analysis/
├── README.md
├── Sprint_5_Analisis_de_Movilidad.ipynb
└── datasets/                         # agregar localmente
    ├── tomtom_traffic.csv
    └── oecd_city_economy.csv
```
