# Aprendizaje No Supervisado aplicado al consumo de sustancias psicoactivas en jóvenes

## Un enfoque nacional con perspectiva territorial en Tierra del Fuego

### Información general

**Materia:** Aprendizaje Automático

**Año:** 2026

**Profesor:** Nicolás Caballero

**Alumna:** Bárbara Jesabel Rigoni

---

## Descripción del proyecto

Este proyecto aplica técnicas de Aprendizaje No Supervisado sobre datos provenientes de la Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas (ENPreCoSP 2011).

El objetivo principal es identificar perfiles de jóvenes argentinos de entre 16 y 24 años mediante algoritmos de clustering, considerando factores sociodemográficos, familiares, territoriales y de salud asociados al consumo de sustancias psicoactivas.

Además, se realiza un análisis específico para la Provincia de Tierra del Fuego, permitiendo una perspectiva territorial complementaria al análisis nacional.

---

## Objetivos

### Objetivo general

Identificar perfiles diferenciados de jóvenes de 16 a 24 años mediante técnicas de agrupamiento no supervisado.

### Objetivos específicos

- Analizar características sociodemográficas y contextuales.
- Reducir dimensionalidad mediante PCA.
- Aplicar algoritmos de clustering.
- Evaluar la calidad de los grupos obtenidos.
- Comparar los perfiles encontrados con los patrones de consumo observados.

---

## Dataset

### Fuente principal

ENPreCoSP 2011 — Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas.

Organismos responsables:

- INDEC
- SEDRONAR
- Observatorio Argentino de Drogas (OAD)

### Cobertura

| Indicador | Valor |
|-----------|--------|
| Registros totales | 34.343 |
| Jóvenes 16-24 años | 6.592 |
| Casos Tierra del Fuego | 265 |
| Variables originales | 291 |

---

## Variables utilizadas para clustering

| Variable | Categoría |
|-----------|-----------|
| BHCH04 | Sexo |
| BHCH05 | Edad |
| NIVINSTR | Nivel educativo |
| CONDACT | Condición de actividad |
| TIPO_H | Tipo de hogar |
| NBI_TOTAL | Necesidades Básicas Insatisfechas |
| RANGOING | Ingreso del hogar |
| BISG01 | Salud general |
| BISG04 | Atención en salud mental |
| BIAC01 | Conoce consumidores cercanos |
| BIAC02 | Cantidad de consumidores cercanos |
| BIAC03 | Curiosidad por probar drogas |
| BIAC04 | Acceso percibido a drogas |
| REGION | Región estadística |
| POB_URB | Tamaño del aglomerado |
| PRVNC | Provincia |

---

## Metodología

### 1. Preprocesamiento

- Limpieza de datos.
- Tratamiento de valores faltantes.
- Codificación de variables categóricas.
- Estandarización de variables.

### 2. Reducción de dimensionalidad

Se aplica Análisis de Componentes Principales (PCA) para:

- Reducir la cantidad de dimensiones.
- Facilitar la visualización.
- Minimizar redundancias.

### 3. Clustering

Se evalúan técnicas de agrupamiento como:

- K-Means
- Clustering Jerárquico

### 4. Evaluación

Métricas utilizadas:

- Silhouette Score
- Davies-Bouldin Index

---

## Resultados preliminares

Los resultados muestran la existencia de perfiles diferenciados de jóvenes según:

- Condiciones socioeconómicas.
- Contexto familiar.
- Entorno de consumo.
- Accesibilidad percibida a sustancias.

---

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Estructura del proyecto

```text
data/
notebooks/
src/
reports/
images/
```

---

## Referencias

- INDEC
- SEDRONAR
- Observatorio Argentino de Drogas
- MedlinePlus (NIH)

---

## Licencia

Los datos utilizados son de dominio público y provienen del Portal de Datos Abiertos de la República Argentina.
