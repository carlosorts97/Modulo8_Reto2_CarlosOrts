# Modulo8_Reto2_CarlosOrts

Proyecto de Ciencia de Datos Reproducible: Análisis y Visualización del Autoempleo (1991-2019)

## 1. Audiencia y contexto

Este proyecto está dirigido a investigadores en Psicología y Sociología interesados en temáticas laborales, bienestar y estructura social. Aunque su formación no es estrictamente económica, estos profesionales buscan comprender las dinámicas del autoempleo desde una perspectiva contextual, integrando tendencias laborales en estudios sobre precariedad, motivación laboral o diferencias culturales entre regiones.

El público tiene un nivel intermedio en visualización de datos, familiarizado con gráficos estáticos en herramientas como SPSS, R o Excel, pero con experiencia limitada en dashboards interactivos. El proyecto prioriza un diseño intuitivo, con elementos explicativos y navegación sencilla, adecuado para uso académico en ordenadores personales, proyecciones en congresos y sesiones colaborativas.

## 2. Preguntas que se pretende responder

El análisis y visualización buscan responder las siguientes preguntas clave:

1. ¿Qué regiones o continentes presentan mayores tasas de autoempleo a lo largo del tiempo?

2. ¿Cómo ha evolucionado el porcentaje de trabajadores por cuenta propia en distintos países desde 1990?

3. ¿Existen correlaciones entre el nivel de autoempleo y variables socioeconómicas como el PIB per cápita?

4. ¿Qué diferencias se observan entre continentes en cuanto a la proporción de trabajadores autónomos?

Estas preguntas guían el diseño del dashboard, asegurando que cada gráfico aporte información relevante y complementaria para una exploración analítica de calidad y contextualizada.

## 3. Objetivo del proyecto

### Objetivo principal:
- Analizar y visualizar de manera interactiva las tendencias del autoempleo a nivel mundial y regional, permitiendo a investigadores comprender patrones socioeconómicos y culturales, y relacionarlos con variables como el PIB per cápita. (Los datos utilizados han sido obtenidos de [www.gapminder.com](https://www.gapminder.org/))

### Objetivos específicos:

- Depurar y preparar los datos de autoempleo y variables socioeconómicas para análisis reproducible.

- Recodificar y generar variables relevantes que faciliten comparaciones entre países, continentes y años.

- Explorar la evolución temporal y regional del autoempleo desde 1990 hasta la fecha disponible.

- Analizar correlaciones entre el porcentaje de trabajadores por cuenta propia y variables socioeconómicas como PIB per cápita.

- Diseñar un dashboard interactivo que permita filtrar por país, continente y año, mostrando gráficos y tablas de manera intuitiva.

- Generar informes técnicos y presentaciones reproducibles que resuman los hallazgos más relevantes y respondan a las preguntas clave de la audiencia.

## 4. Estructura del proyecto

```plaintext
├── dashboard
│   ├── dashboard.html
│   └── dashboard.Rmd
├── datos
│   ├── data_base.csv
│   ├── gdp_pcap.csv
│   ├── self_employed_percent_of_employment.csv
│   └── Transformacion_de_Datos.Rmd
├── informe
│   ├── img
│   │   ├── boxplot_continentes_1991.png
│   │   ├── boxplot_continentes_2019.png
│   │   ├── evolución_por_pais_espana.png
│   │   ├── linea_temportal_continentes.png
│   │   ├── mapa_mundo.png
│   │   ├── pib_vs_autonomos_1991.png
│   │   ├── pib_vs_autonomos_2019.png
│   │   ├── top_bottom_10_1991.png
│   │   └── top_bottom_10_2019.png
│   ├── informe.html
│   ├── informe.pdf
│   └── informe.Rmd
├── Modulo8_Reto2_CarlosOrts.Rproj
├── presentacion
│   ├── estilo.css
│   ├── presentacion.html
│   ├── presentacion.log
│   ├── presentacion.Rmd
│   └── presentacion.tex
└── README.md
```

## 5. Requisitos e instalación

El proyecto está desarrollado en **R (≥4.0)** con soporte para **RMarkdown**.  

### Paquetes principales utilizados:
- tidyverse
- dplyr
- ggplot2
- plotly
- knitr
- flexdashboard / shiny
- readr
- haven
- tidyr
- countrycode
- maps
- DT
- rmarkdown
- forcats
 
## Reproducir el entorno
Para instalar todos los paquetes necesarios:

```r
paquetes <- c(
  "readr", "haven", "dplyr", "tidyr", "countrycode",
  "flexdashboard", "tidyverse", "shiny", "maps",
  "DT", "ggplot2", "rmarkdown", "forcats", "knitr"
)

for(p in paquetes){
  if(!require(p, character.only = TRUE)){
    install.packages(p, dependencies = TRUE)
    library(p, character.only = TRUE)
  }
}
```

## 6. Instrucciones de uso
Una guía rápida para que cualquiera pueda reproducirlo:

1. Clonar el repositorio:  
   ```bash
   git clone https://github.com/tuusuario/Modulo8_Reto2_CarlosOrts.git
2. Abrir el archivo Modulo8_Reto2_CarlosOrts.Rproj en RStudio.
3. Ejecutar Transformacion_de_Datos.Rmd para preparar los datos.
4. Renderizar informe/informe.Rmd para generar el informe en PDF/HTML.
5. Abrir dashboard/dashboard.Rmd y correrlo para visualizar el dashboard interactivo.

## 7. Resultados principales

- África presenta las tasas más altas de autoempleo, Europa las más bajas.  
- Tendencia global decreciente del autoempleo (1991–2019).  
- Relación negativa entre autoempleo y PIB per cápita.  

📄 Informe completo: [`informe/informe.pdf`](informe/informe.pdf)  
📊 Dashboard interactivo: [`dashboard/dashboard.html`](dashboard/dashboard.html)

## 8. Autores y créditos
Proyecto realizado por **Carlos Orts** en el marco del *Módulo 8 – 'Data visualization' y 'Reproducibility'*.  

