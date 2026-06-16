---
 
![Portada del proyecto](images/portada_tdf_v5.svg)


---
![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-yellow)
![Estado](https://img.shields.io/badge/Estado-Completado-brightgreen)
![Licencia](https://img.shields.io/badge/Licencia-Dominio%20P%C3%BAblico-lightgrey)

---

## 📌 Descripción del Proyecto

Este proyecto aplica técnicas de **Aprendizaje Automático No Supervisado** para identificar y caracterizar perfiles naturales de consumo de sustancias psicoactivas en jóvenes de 16 a 24 años de Argentina, con un análisis comparativo específico para la **Provincia de Tierra del Fuego, Antártida e Islas del Atlántico Sur**.

A diferencia de los enfoques tradicionales que imponen categorías predefinidas, este proyecto permite que sean los propios datos quienes revelen los patrones subyacentes, evitando sesgos en la clasificación del riesgo.

---

## 🎯 Objetivo General

Identificar automáticamente perfiles de consumo de sustancias psicoactivas en jóvenes de entre 16 y 24 años de Argentina, por medio de técnicas de Aprendizaje No Supervisado, y analizar comparativamente los patrones identificados en la Provincia de Tierra del Fuego respecto del resto del país.

---

## 🗂️ Estructura del Repositorio

```
Parcial-Aprendizaje-Automatico/
│
├── README.md
├── images/
│   └── portada_tdf_v5.svg
│
├── data/
│   ├── raw/                          ← Datasets originales sin modificar
│   │   ├── Base_Usuario_ENPreCoSP-2011.txt
│   │   └── base_usuario_encoprac2022.txt
│   └── processed/                    ← Datos filtrados y listos para usar
│       ├── ENPreCoSP_2011_jovenes_16_24.csv
│       └── ENCoPraC_2022_jovenes_16_24.csv
│
├── notebooks/                        ← Notebooks Jupyter del proyecto
│   └── Rigoni_Barbara_Parcial.ipynb
|   └── Portada.ipynb
│
├── docs/                             ← Documentación del proyecto 
│   ├── entrega.md
│   ├── manuales.md
|
├── reports/
│   └── figures/                      ← Gráficos y visualizaciones
│   
├── video/                            ← Video explicativo del proyecto
│   └── link.md
|
└── references/                       ← Fuentes y bibliografía
    └── referencias.md
    
```

---

## 📊 Datasets

### Dataset Principal — ENPreCoSP 2011
| Característica | Valor |
|---|---|
| **Nombre** | Encuesta Nacional sobre Prevalencias de Consumo de Sustancias Psicoactivas |
| **Organismo** | INDEC / Ministerio de Salud / SEDRONAR |
| **Año** | 2011 |
| **Registros totales** | 34.343 |
| **Variables** | 291 |
| **Subconjunto del proyecto (16-24 años)** | 6.592 registros |
| **Subconjunto Tierra del Fuego (16-24 años)** | 265 registros |
| **Fuente** | [indec.gob.ar](https://www.indec.gob.ar/indec/web/Institucional-Indec-BasesDeDatos-2) |
| **Licencia** | Dominio público |

### Dataset Complementario — ENCoPraC 2022
| Característica | Valor |
|---|---|
| **Nombre** | Encuesta Nacional sobre Consumos y Prácticas de Cuidado |
| **Organismo** | SEDRONAR / INDEC |
| **Año** | 2022 |
| **Registros totales** | 12.062 |
| **Subconjunto (16-24 años)** | 1.798 registros |
| **Variables** | 562 |
| **Fuente** | [indec.gob.ar](https://www.indec.gob.ar/indec/web/Institucional-Indec-BasesDeDatos-2) |

> El análisis principal se desarrolló sobre la ENPreCoSP 2011, mientras que la ENCoPraC 2022 se utilizó exclusivamente para una comparación descriptiva de la evolución temporal de las prevalencias de consumo.

---

## 🤖 Técnicas de Aprendizaje Automático

| Técnica | Rol en el proyecto |
|---|---|
| **K-Means** | Descubrimiento de grupos naturales de jóvenes |
| **DBSCAN** | Complementación del clustering y detección de outliers |
| **PCA** | Reducción de dimensionalidad y visualización |
| **Random Forest** | Validación complementaria de los perfiles identificados e interpretación de la importancia de variables |

### Métricas de evaluación
- Coeficiente de Silhouette
- Índice de Davies-Bouldin
- Método del Codo
- Accuracy (Random Forest)
- Matriz de confusión (Random Forest)
---

## 🔬 Principales Hallazgos

Los resultados obtenidos permitieron identificar una estructura consistente de tres perfiles de consumo diferenciados. Posteriormente, estos perfiles fueron comparados entre el conjunto nacional y la provincia de Tierra del Fuego, revelando diferencias territoriales significativas.

### Perfiles descubiertos
| Perfil | Proporción | Características |
|---|---|---|
| 🟢 Bajo consumo | 60,1% | Consumo moderado de alcohol |
| 🔴 Alto consumo | 30,2% | Alcohol, tabaco y marihuana elevados |
| 🟡 Consumo moderado | 9,7% | Alcohol y tabaco sin sustancias ilícitas |

### Tierra del Fuego vs Nacional
| Indicador | Nacional | TDF |
|---|---|---|
| Cluster alto consumo | 30,2% | **51,3%** |
| Alcohol | 67,4% | **73,6%** |
| Tabaco | 32,4% | **40,0%** |
| Marihuana | 4,3% | **6,0%** |

### Variables más influyentes
1. 🥇 Acceso a drogas
2. 🥈 Conocer consumidores cercanos
3. 🥉 Curiosidad por probar drogas
4. Ingreso del hogar

### Conclusión

El estudio permitió identificar tres perfiles diferenciados de consumo y mostró que la provincia de Tierra del Fuego presenta una proporción considerablemente mayor de jóvenes pertenecientes al perfil de alto consumo respecto del promedio nacional. Asimismo, las variables vinculadas al entorno social demostraron una mayor capacidad para diferenciar los perfiles que otros indicadores socioeconómicos tradicionales.

---

## 🛠️ Tecnologías

```python
# Librerías principales
pandas          # Manipulación de datos
numpy           # Operaciones numéricas
scikit-learn    # Modelos de ML
matplotlib      # Visualizaciones
seaborn         # Visualizaciones estadísticas
```

## 🎬 Video explicativo
El video de presentación del proyecto está disponible en [`video/link.md`](video/link.md).

---

## 📚 Referencias

- INDEC / Ministerio de Salud (2011). *ENPreCoSP 2011*. Buenos Aires: INDEC.
- SEDRONAR / INDEC (2022). *ENCoPraC 2022*. Buenos Aires: SEDRONAR.
- MedlinePlus / NIH (2025). *Trastorno de consumo de drogas — Factores de riesgo*.
- Rousseeuw, P.J. (1987). *Silhouettes: a graphical aid to the interpretation and validation of cluster analysis*. Journal of Computational and Applied Mathematics, 20, 53-65.
- Observatorio Argentino de Drogas — SEDRONAR. *Informes de prevalencias de consumo en población joven*.

---

## ⚖️ Consideraciones Éticas

Los datos utilizados provienen de una encuesta oficial de dominio público, anonimizada y sin datos personales identificables, en cumplimiento con la **Ley N° 17.622 de Resguardo del Secreto Estadístico**.

---

## 📌 Aporte del trabajo

Este proyecto muestra el potencial del Aprendizaje Automático No Supervisado para el estudio de fenómenos sociales complejos. La combinación de técnicas de clustering, reducción de dimensionalidad e interpretación de variables permitió identificar perfiles de consumo y analizar diferencias territoriales que no resultan evidentes mediante enfoques descriptivos tradicionales.

Los resultados constituyen una aproximación exploratoria que puede servir como punto de partida para futuras investigaciones y para el diseño de estrategias de prevención basadas en evidencia.

---

*Materia: Aprendizaje Automático | Alumna: Bárbara Jesabel Rigoni | Profesor: Nicolás Caballero | 2026*
