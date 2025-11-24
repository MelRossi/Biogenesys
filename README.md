# 🐍 Proyecto Integrador: Expansión Estratégica de Biogenesys con Python

## 🧬 Análisis Epidemiológico, Demográfico y Económico en Latinoamérica

**Autora:** Melisa Rossi | **Curso:** Data Analytics - Henry |

---

## 📝 Introducción y Objetivos

La empresa **BIOGENESYS**, dedicada a la investigación y desarrollo farmacéutico, se encuentra en un proceso de expansión estratégica en Latinoamérica.

El objetivo principal de este proyecto es determinar las **ubicaciones óptimas** para nuevos laboratorios farmacéuticos en seis países clave: **Argentina, Brasil, Chile, Colombia, México y Perú**. El análisis se basa en datos sobre incidencia de COVID-19, vacunación, y factores demográficos, económicos y sanitarios

Se busca:
* Evaluar el impacto de la pandemia y sus factores correlacionados.
* Comprender las relaciones entre las variables e identificar patrones estructurales entre los países.
* Minimizar riesgos operativos y maximizar el potencial de mercado para la expansión.

---

## 🛠️ Tecnologías y Herramientas

| Categoría | Herramientas Utilizadas | Uso Principal |
| :--- | :--- | :--- |
| **Análisis y Transformación** | Python (Pandas, NumPy) | Limpieza de datos, normalización, filtrado y generación de estadísticas descriptivas. |
| **Visualización Estática** | Matplotlib y Seaborn  | Análisis Exploratorio de Datos (EDA) con histogramas, mapas de calor, boxplots y diagramas de dispersión. |
| **Visualización Interactiva** | Power BI  | Creación de un dashboard dinámico para la exploración de resultados. |

---

## ⚙️ Desarrollo del Proyecto: Limpieza y Transformación (Python)

El proyecto se inició cargando el archivo `data_latinoamerica.csv` y aplicando filtros estratégicos para concentrar el análisis en los seis países de interés y en las fechas posteriores al 1 de enero de 2021.

### Proceso de Normalización y Limpieza:

* **Eliminación de Columnas:** Se eliminaron las columnas `"new_recovered"` y `"cumulative_recovered"` , ya que los valores nulos superaban el 50% de los datos.
* **Imputación de Nulos:**
    * Valores nulos en columnas de casos y muertes se rellenaron con **"0"**.
    * Para dosis de vacunas acumuladas y variables climáticas, se aplicó **Forward Fill** (último valor conocido).
    * Para el nulo restante en `"rainfall_mm"`, se aplicó **Backward Fill** (primer valor no nulo).
* **Transformación de Tipos de Datos:** La columna `"date"` se convirtió a tipo fecha, y las columnas categóricas se transformaron a tipo `category`0]. Las columnas numéricas referentes a población pasaron de `float64` a `int64`.

**Resultado:** Se obtuvo un DataFrame limpio, sin valores faltantes y estructuralmente optimizado, listo para el análisis.

---

## 🔎 Análisis Exploratorio de Datos (EDA) e Insights

El EDA se centró en caracterizar las condiciones demográficas, sanitarias, económicas y epidemiológicas.

### Hallazgos Clave por País:

* **Brasil:** Lidera las cifras absolutas de contagios, muertes y vacunación, lo cual se relaciona con su gran tamaño poblacional.
* **Chile:** Destaca por su mayor **PIB per cápita**, baja tasa de mortalidad infantil y mayor expectativa de vida, posicionándose como un referente en eficiencia de gestión sanitaria.
* **México:** Combina una alta incidencia de casos con una mortalidad elevada y presenta la densidad poblacional más alta. [cite_start]Lidera en prevalencia de **diabetes** (13,5%).
* **Argentina:** Muestra alta variabilidad en indicadores, pero con una mortalidad controlada. Se destaca por una mayor urbanización y menor densidad poblacional.

### Relaciones Clave (Correlaciones):

* Existe una correlación positiva fuerte (≥ 0,8) entre variables demográficas (ej. Población) y las cifras acumuladas de casos y muertes.
* La correlación entre la población urbana y los casos confirmados (0,77) fue más alta que la rural (0,55).
* La **temperatura promedio no parece ser un predictor fuerte** de la cantidad de nuevos casos; más bien define el rango en el que se mueve la pandemia en cada país.

### Análisis Temporal:

* **Patrón Estacional:** Todos los países compartieron un patrón con **dos grandes picos epidémicos**: uno a mediados de 2021 y otro más pronunciado a inicios de 2022].
* **Efecto Vacunación:** Las muertes mostraron una tendencia decreciente sostenida desde mediados de 2021]. A pesar del incremento en contagios en 2022, las muertes no aumentaron proporcionalmente, evidenciando el efecto protector de la inmunización.

---

## 💡 Recomendaciones Estratégicas (Biogenesys)

Basado en el análisis, se recomiendan las siguientes estrategias de expansión:

* **Priorización Geográfica Inmediata:** Dirigir la expansión inicial hacia **Brasil, Chile y Argentina**, debido al volumen de mercado y la estabilidad sanitaria.
* **Segmentación Sanitaria:** Diseñar productos y programas enfocados en **diabetes, enfermedades respiratorias y cardiovasculares**, dadas sus prevalencias significativas en la región.
* **Enfoque Logístico:** Aprovechar la **alta concentración urbana** para optimizar la cadena de suministro y distribución de productos farmacéuticos.
* **Oportunidades a Mediano Plazo:** En **Perú y Colombia**, impulsar alianzas estratégicas para el refuerzo de la infraestructura sanitaria, lo que amplía la presencia regional.

---

## ✍️ Reflexión Personal

Este proyecto consolidó la comprensión de que el rol del analista de datos no se limita al procesamiento técnico, sino que es un puente entre los datos y la toma de decisiones estratégicas. El desafío principal fue interpretar los datos desde una perspectiva estratégica, conectando los hallazgos con la realidad sanitaria, económica y social de Latinoamérica.
