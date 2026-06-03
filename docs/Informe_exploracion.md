# Descripción del Dataset y Origen

**Materia:** Aprendizaje Automático  
**Año:** 2026  
**Profesor:** Nicolás Caballero  
**Alumna:** Bárbara Jesabel Rigoni  

---

> *"Aprendizaje No Supervisado aplicado al consumo de sustancias psicoactivas en jóvenes: un enfoque Nacional con perspectiva territorial en Tierra del Fuego"*

---

## 1. Origen del Dataset

### Dataset principal: ENPreCoSP 2011

La Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas (ENPreCoSP 2011) fue elaborada en conjunto por el Ministerio de Salud de la Nación, a través de la Dirección de Salud Mental y Adicciones, el Instituto Nacional de Estadística y Censos (INDEC) y las Direcciones Provinciales de Estadísticas. Su objetivo fue actualizar el sistema de información sobre el consumo de sustancias psicoactivas a nivel nacional para el diseño de políticas públicas más eficaces.

| Campo | Detalle |
|---|---|
| **Organismo productor** | INDEC / Ministerio de Salud de la Nación / SEDRONAR |
| **Período de relevamiento** | Agosto a octubre de 2011 |
| **Fecha de adquisición** | Mayo 2026 |
| **Fuente de descarga** | https://www.indec.gob.ar/indec/web/InstitucionalIndec-BasesDeDatos-2 |
| **Formato del archivo** | Texto plano delimitado por pipes (`\|`) — `Base_Usuario_ENPreCoSP-2011.txt` |
| **Licencia** | Dominio público — datos abiertos del Estado Argentino |

---

## 2. Descripción Completa del Dataset Principal (ENPreCoSP 2011)

### 2.1 Dimensiones generales

| Característica | Dataset completo | Subconjunto del proyecto (jóvenes 16-24 años) | Subconjunto TDF (16-24 años) |
|---|---|---|---|
| Instancias (filas) | 34.343 | 6.592 | 265 |
| Variables (columnas) | 291 | 291 | 291 |
| Separador | Pipe (`\|`) | Pipe (`\|`) | Pipe (`\|`) |
| Codificación | Latín-1 | Latín-1 | Latín-1 |
| Tipo de datos | int64 / float64 | int64 / float64 | int64 / float64 |

### 2.2 Población objetivo y cobertura

La encuesta relevó personas de 16 a 65 años residentes en viviendas particulares ubicadas en localidades urbanas de 5.000 y más habitantes de la República Argentina. El diseño muestral es probabilístico y multietápico (la selección se hace en varias etapas consecutivas), contemplando 4 etapas de selección: departamento, área, vivienda e individuo, mediante tabla de Kish (método estandarizado y aleatorio, utilizado para evitar sesgos). Permite estimaciones a nivel de 24 jurisdicciones, 6 regiones estadísticas y 4 agrupamientos de poblaciones urbanas.

Para este proyecto se trabajará con el subconjunto de jóvenes de 16 a 24 años (`GRUPEDAD = 2`), que comprende **6.592 registros a nivel nacional** y **265 registros correspondientes a la Provincia de Tierra del Fuego** (`PRVNC = 94`).

### 2.3 Perfil del subconjunto de trabajo (jóvenes 16-24 años, nacional)

| Variable | Descripción | Distribución |
|---|---|---|
| Sexo | Varón / Mujer | Varón: 3.169 (48,1%) \| Mujer: 3.423 (51,9%) |
| Edad | 16 a 24 años | Promedio: 20,1 años \| Mín: 16 \| Máx: 24 |
| Alcohol (último año) | P1A_BA | 4.444 consumidores (67,4%) |
| Tabaco (último año) | P1A_TA | 2.139 consumidores (32,4%) |
| Marihuana (último año) | P1A_MA | 283 consumidores (4,3%) |
| Cocaína (último año) | P1A_CO | 61 consumidores (0,9%) |
| Pasta base (último año) | P1A_PB | 4 consumidores (0,1%) |
| Tranquilizantes (último año) | P1A_TR | 74 consumidores (1,1%) |

---

## 3. Variables Seleccionadas para el Proyecto

### 3.1 Variables para el agrupamiento (clustering)

Las siguientes 16 variables serán utilizadas como insumo para las técnicas de Aprendizaje No Supervisado. Su selección está fundamentada en los factores de riesgo documentados por MedlinePlus (NIH) y el Observatorio Argentino de Drogas (SEDRONAR).

| Variable | Descripción | Categoría | Valores únicos | Nulos/Ns |
|---|---|---|---|---|
| `BHCH04` | Sexo | Sociodemográfica | 2 | 0 |
| `BHCH05` | Edad en años cumplidos | Sociodemográfica | 9 | 0 |
| `NIVINSTR` | Nivel de instrucción | Sociodemográfica | 8 | 0 |
| `CONDACT` | Condición de actividad | Sociodemográfica | 3 | 0 |
| `TIPO_H` | Tipo de hogar | Contexto familiar | 8 | 0 |
| `NBI_TOTAL` | Necesidades Básicas Insatisfechas | Contexto familiar | 5 | 0 |
| `RANGOING` | Rango de ingreso del hogar | Contexto familiar | 19 | 964 |
| `BISG01` | Autopercepción de salud general | Salud y entorno | 5 | 0 |
| `BISG04` | Visita profesional de salud mental | Salud y entorno | 2 | 12 |
| `BIAC01` | Conoce consumidores cercanos | Salud y entorno | 2 | 20 |
| `BIAC02` | Cantidad de consumidores cercanos | Salud y entorno | 3 | 3.991 |
| `BIAC03` | Curiosidad por probar drogas | Salud y entorno | 3 | 20 |
| `BIAC04` | Posibilidad de acceso a drogas | Salud y entorno | 2 | 19 |
| `REGION` | Región estadística del país | Territorial | 6 | 0 |
| `POB_URB` | Tamaño de aglomerado urbano | Territorial | 4 | 0 |
| `PRVNC` | Provincia de residencia | Territorial | 24 | 0 |

### 3.2 Variables de consumo (análisis descriptivo y comparativo)

| Variable | Sustancia | Consumidores (último año) | Porcentaje |
|---|---|---|---|
| `P1A_BA` | Bebidas alcohólicas | 4.444 | 67,4% |
| `P1A_TA` | Tabaco | 2.139 | 32,4% |
| `P1A_MA` | Marihuana | 283 | 4,3% |
| `P1A_CO` | Cocaína | 61 | 0,9% |
| `P1A_PB` | Pasta base | 4 | 0,1% |
| `P1A_TR` | Tranquilizantes sin receta | 74 | 1,1% |

---

## 4. Proceso de Recopilación y Preprocesamiento Inicial

El dataset fue descargado desde el Portal de Datos Abiertos del INDEC en formato de texto plano. Para su utilización en el proyecto se realizaron los siguientes pasos de preprocesamiento inicial:

1. Descompresión del archivo RAR (`bases_enprecosp2011.rar`) y extracción del archivo de texto plano (`Base_Usuario_ENPreCoSP-2011.txt`).
2. Carga del dataset en Google Colaboratory utilizando pandas con los parámetros `sep='|'` y `encoding='latin-1'` para respetar el separador original y la codificación de caracteres en español.
3. Filtrado del subconjunto de jóvenes de 16 a 24 años (`GRUPEDAD = 2`), obteniendo 6.592 registros a nivel nacional.
4. Identificación del subconjunto de Tierra del Fuego (`PRVNC = 94`), obteniendo 265 registros.
5. Consulta del Documento para la Utilización de la Base de Datos Usuario (`enprecosp_2011_documento_baseusuario.pdf`) para interpretar la codificación de cada variable y sus valores válidos.
6. Identificación de valores faltantes y códigos de no respuesta (códigos 9, 99, 999 según el diccionario) para su tratamiento en la etapa de preprocesamiento formal.

El preprocesamiento completo —imputación de valores faltantes, codificación de variables categóricas, normalización— más la aplicación de Análisis de Componentes Principales (PCA), con el objetivo de reducir la dimensionalidad de las 16 variables seleccionadas y representar gráficamente la distribución de los jóvenes para facilitar la interpretación visual de los clusters obtenidos, se desarrollará en la Entrega 3 mediante una notebook de Python en el repositorio GIT.

---

## 5. Fuente de Datos

**Fuente principal:**  
ENPreCoSP 2011 — Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas.  
Organismo: INDEC / SEDRONAR / Observatorio Argentino de Drogas (OAD).  
Registros totales: 34.343 | Jóvenes 16-24 años: 6.592 | Subconjunto TDF: 265 registros.  
Variables disponibles: 291.  
Disponible en: (https://www.indec.gob.ar/indec/web/InstitucionalIndec-BasesDeDatos-2)

---

*Materia: Aprendizaje Automático | Alumna: Bárbara Jesabel Rigoni | Profesor: Nicolás Caballero | 2026*
