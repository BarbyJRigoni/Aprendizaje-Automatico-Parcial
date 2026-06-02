# Aprendizaje No Supervisado aplicado al consumo de sustancias psicoactivas en jóvenes
### Un enfoque Nacional con perspectiva territorial en Tierra del Fuego

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-yellow)
![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-green)

---

## Descripción del Proyecto

Este proyecto aplica técnicas de **Aprendizaje Automático No Supervisado** para identificar y caracterizar perfiles naturales de consumo de sustancias psicoactivas en jóvenes de 16 a 24 años de Argentina, con un análisis comparativo específico para la **Provincia de Tierra del Fuego, Antártida e Islas del Atlántico Sur**.

A diferencia de los enfoques tradicionales que imponen categorías predefinidas, este proyecto propone que los propios datos revelen patrones sin sesgos previos.

---

## Objetivo General

Identificar automáticamente perfiles de consumo de sustancias psicoactivas en jóvenes de entre 16 y 24 años de Argentina, por medio de técnicas de Aprendizaje No Supervisado, y analizar comparativamente los patrones identificados en la Provincia de Tierra del Fuego respecto del resto del país.

---

## Estructura del Repositorio

```
Parcial-Aprendizaje-Automatico/
│
├── README.md                        
│
├── data/
│   ├── raw/                         
│   │   ├── Base_Usuario_ENPreCoSP-2011.txt
│   │   └── base_usuario_encoprac2022.txt (en analisis para uso final)
│   └── processed/                   
│
├── notebooks/                       
│
├── docs/                            
│   ├── Parcial-Entrega_1.pdf
│   └── Parcial-Entrega_2.pdf
│
├── src/                             
│
└── references/                      
    └── enprecosp_2011_documento_baseusuario.pdf
```

---

## Datasets

### Dataset Principal — ENPreCoSP 2011
| Característica | Valor |
|---|---|
| Nombre | Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas |
| Organismo | INDEC / Ministerio de Salud / SEDRONAR |
| Año | 2011 |
| Registros totales | 34.343 |
| Variables | 291 |
| Subconjunto del proyecto (16-24 años) | 6.592 registros |
| Subconjunto Tierra del Fuego (16-24 años) | 265 registros |
| Fuente | (https://www.indec.gob.ar/indec/web/Institucional-Indec-BasesDeDatos-2)|
| Licencia | Dominio público |

### Dataset Complementario — ENCoPraC 2022 (en análisis para uso final)
| Característica | Valor |
|---|---|
| Nombre | Encuesta Nacional sobre Consumos y Prácticas de Cuidado |
| Organismo | SEDRONAR / INDEC |
| Año | 2022 |
| Registros totales | 12.062 |
| Variables | 562 |
| Fuente | (https://www.indec.gob.ar/indec/web/Institucional-Indec-BasesDeDatos-2) |

---

## Técnicas de Aprendizaje Automático

| Técnica | Rol en el proyecto |
|---|---|
| **K-Means** | Descubrimiento de grupos naturales de jóvenes |
| **DBSCAN** | Validación de clusters y detección de outliers |
| **PCA** | Herramienta de visualización (reducción de dimensionalidad) |

### Métricas de evaluación
- Coeficiente de Silhouette
- Índice de Davies-Bouldin
- Método del Codo (para K-Means)

---

## Variables del Proyecto

### Variables para el agrupamiento (16 variables)
| Categoría | Variables |
|---|---|
| Sociodemográficas | Sexo, Edad, Nivel de instrucción, Condición de actividad |
| Contexto familiar | Tipo de hogar, NBI, Rango de ingreso |
| Salud y entorno | Autopercepción de salud, Visita a salud mental, Entorno con consumidores, Curiosidad y acceso a drogas |
| Territorial | Región, Tamaño del aglomerado, Provincia |

### Variables de consumo (análisis descriptivo)
`P1A_BA` · `P1A_TA` · `P1A_MA` · `P1A_CO` · `P1A_PB` · `P1A_TR`

---

## Tecnologías

- **Python 3.x**
- **pandas** — manipulación de datos
- **scikit-learn** — modelos de ML
- **matplotlib / seaborn** — visualizaciones
- **Jupyter Notebook** — desarrollo interactivo

---

## Entregas

| Entrega | Descripción | Estado |
|---|---|---|
| Entrega 1 | Descripción y Formulación del Objetivo | ✅ Completada |
| Entrega 2 | Descripción del Dataset y Origen | ✅ Completada |
| Entrega 3 | Modelo, Análisis y Resultados | 🔄 En desarrollo |

---

## Referencias

- INDEC / Ministerio de Salud (2011). *ENPreCoSP 2011 — Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas*. Buenos Aires: INDEC.
- SEDRONAR / INDEC (2022). *ENCoPraC 2022 — Encuesta Nacional sobre Consumos y Prácticas de Cuidado*. Buenos Aires: SEDRONAR. (en analisis para uso final)
- MedlinePlus / NIH (2025). *Trastorno de consumo de drogas — Factores de riesgo*. Disponible en: medlineplus.gov
- Observatorio Argentino de Drogas — SEDRONAR. *Informes de prevalencias de consumo en población joven*.

---

## Consideraciones Éticas

Los datos utilizados provienen de una encuesta oficial de dominio público, anonimizada y sin datos personales identificables, en cumplimiento con la Ley N° 17.622 de Resguardo del Secreto Estadístico.

---

*Materia: Aprendizaje Automático | Alumna: Bárbara Jesabel Rigoni | Profesor: Nicolás Caballero | 2026*
