# Análisis de Pokémon Legendarios

## 📋 Descripción General

Este proyecto realiza un análisis exploratorio y descriptivo de las características estadísticas de los Pokémon, con énfasis en identificar qué atributos distinguen a los Pokémon legendarios del resto de la población. El análisis utiliza un conjunto de datos de 802 Pokémon recolectados hasta la época de la investigación.

---

## 🎯 Objetivo del Análisis

El objetivo principal de este proyecto es **determinar qué habilidades y características deben poseer un Pokémon para ser considerado legendario**. Específicamente, buscamos responder la pregunta:

> *¿Por qué algunos Pokémon que se comparan en fuerza a los Pokémon legendarios no son considerados como tales?*

Para ello, se realiza un análisis multivariado de:
- Puntos de vida (HP)
- Ataque y Defensa
- Ataque y Defensa Especial
- Velocidad
- Características físicas (altura y peso)

---

## 📊 Dataset Utilizado

**Nombre del dataset:** `Puchamon.csv`

### Descripción de Variables

El conjunto de datos contiene información de 802 Pokémon con las siguientes variables:

| Variable | Descripción |
|----------|-------------|
| `pokedex_number` | Identificador único del Pokémon en la Pokédex |
| `name` | Nombre de la especie del Pokémon según su evolución |
| `hp` | Puntos de vida del Pokémon |
| `attack` | Puntos de daño al realizar ataques físicos |
| `defense` | Puntos de vida mantenidos al recibir ataques físicos |
| `sp_attack` | Poder de ataque especial (mágico) |
| `sp_defense` | Capacidad para mitigar ataques especiales |
| `speed` | Velocidad en combate |
| `height_m` | Altura de la especie en metros |
| `weight_kg` | Peso de la especie en kilogramos |
| `is_legendary` | Indicador binario (0: no legendario, 1: legendario) |

### Variables Excluidas del Análisis

Se excluyeron las siguientes variables por considerarlas irrelevantes para determinar si un Pokémon es legendario:
- `percentage_male`: El género no influye en estado legendario
- `type`: El tipo de Pokémon no determina su condición legendaria
- `generation`: La época de descubrimiento es irrelevante para sus habilidades

---

## 🛠️ Herramientas y Tecnologías Utilizadas

### Lenguaje
- **Python 3.x**

### Librerías Principales

| Librería | Propósito |
|----------|-----------|
| **Pandas** | Manipulación, tratamiento y análisis de datos |
| **NumPy** | Cálculos numéricos y operaciones matriciales |
| **Matplotlib** | Visualización gráfica en 2D |
| **Seaborn** | Visualización estadística avanzada |
| **SciPy** | Análisis estadístico y distribuciones |

### Entorno de Ejecución
- Jupyter Notebook / Google Colab

---

## 📈 Principales Hallazgos

### Características de Pokémon Legendarios

#### 1. **Distribución de Estadísticas**
- Los Pokémon legendarios presentan valores **significativamente superiores** en todas las estadísticas comparadas con Pokémon normales
- Especialmente destacados en: **HP**, **Ataque Especial** y **Defensa Especial**

#### 2. **Análisis Descriptivo**
- **Cantidad de Legendarios:** 143 de 802 Pokémon (17.8%)
- **Media de HP en Legendarios:** Sustancialmente mayor que en normales
- **Distribución:** Las estadísticas de Pokémon legendarios muestran mayor concentración en valores altos

#### 3. **Variables Críticas**
Los análisis revelan que las estadísticas de combate (HP, ataque, defensa y sus variantes especiales) son los mejores predictores del estatus legendario, explicando por qué algunos Pokémon "pseudo-legendarios" se comparan en fuerza pero no tienen la clasificación oficial.

#### 4. **Correlaciones**
- Existe correlación positiva entre variables de ataque y defensa
- Los Pokémon legendarios ocupan el extremo superior de la distribución multivariada

---

## 📂 Estructura del Proyecto

```
proyecto-análisis-de-datos/
├── README.md                              # Este archivo
├── Puchamon.csv                          # Dataset principal
├── Puchamon_final_PTM.ipynb             # Análisis principal (recomendado)
├── Análisis_de_datos.ipynb              # Análisis alternativo
└── [Otros notebooks]
```

### Notebook Recomendado
**`Puchamon_final_PTM.ipynb`** - Contiene el análisis completo y bien estructurado con:
- Importación y limpieza de datos
- Análisis descriptivo detallado
- Visualizaciones profesionales
- Comparativas entre Pokémon legendarios y no legendarios

---

## 🔍 Metodología

### Pasos del Análisis

1. **Importación de Datos**
   - Carga del dataset CSV
   - Validación de integridad

2. **Limpieza de Datos**
   - Eliminación de variables irrelevantes
   - Reorganización de columnas por relevancia
   - Verificación de datos faltantes

3. **Análisis Descriptivo**
   - Cálculo de estadísticas de resumen (media, desv. estándar, cuartiles, moda)
   - Análisis por grupos (legendarios vs. no legendarios)

4. **Visualización Exploratoria**
   - Diagramas de caja (box plots)
   - Gráficos de densidad
   - Histogramas de distribución
   - Correlogramas

5. **Análisis Comparativo**
   - Comparación estadística entre grupos
   - Identificación de diferencias significativas

---

## 🚀 Cómo Ejecutar el Proyecto

### Requisitos Previos
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### Ejecución
1. Abre Jupyter Notebook o Google Colab
2. Carga el archivo `Puchamon_final_PTM.ipynb`
3. Ejecuta las celdas en orden secuencial

**Nota:** El dataset se carga directamente desde el repositorio de GitHub, no requiere descarga previa.

---

## 💡 Principales Insights

1. **Diferenciación Clara:** Los Pokémon legendarios se diferencian significativamente por sus estadísticas de combate, no por características físicas o género.

2. **Pseudolegendarios:** Existen Pokémon con estadísticas muy similares a legendarios pero sin la clasificación oficial, posiblemente por razones narrativas o de diseño del juego.

3. **Multidimensionalidad:** La condición de "legendario" no depende de una única variable, sino de un conjunto de características elevadas simultáneamente.

4. **Distribución Poblacional:** Los legendarios representan una pequeña fracción (18%) de la población total, formando un grupo altamente especializado.

---

## 🔮 Mejoras Futuras

1. **Modelos Predictivos**
   - Implementar clasificadores (Logistic Regression, Random Forest)
   - Crear modelos de predicción de estado legendario
   - Evaluar importancia de características

2. **Análisis Avanzado**
   - Análisis de componentes principales (PCA)
   - Clustering de Pokémon por similitud
   - Análisis de serie temporal por generación

3. **Visualizaciones Mejoradas**
   - Investigar Pokémon "en la frontera" (pseudo-legendarios)
   - Análisis de impacto por tipo
   - Comparativas por generación

4. **Documentación Adicional**
   - Análisis de datos faltantes
   - Pruebas de normalidad
   - Análisis de varianza (ANOVA)

---

## 📝 Notas Académicas

Este proyecto fue realizado con fines académicos enfocándose en los **fundamentos del análisis exploratorio de datos**. El énfasis está en la comprensión de conceptos estadísticos básicos y técnicas de visualización, no en la creación de modelos predictivos complejos.

### Principios Mantenidos
- ✅ Sin cambios en el dataset original
- ✅ Sin modelos de machine learning avanzados
- ✅ Análisis descriptivo e interpretativo
- ✅ Enfoque en claridad y correcta presentación

---

## 👤 Información del Proyecto

- **Tipo:** Análisis Exploratorio de Datos (EDA)
- **Dominio:** Ciencia de Datos / Business Intelligence
- **Nivel:** Fundamentals/Intermedio
- **Dataset:** Pokémon Legendarios (802 registros)
- **Estado:** Completado

---

## 📞 Contacto y Referencias

Para dudas sobre el análisis o mejoras sugeridas en la metodología, consulta las celdas de documentación en los notebooks incluidos en el proyecto.

---

**Última actualización:** Febrero 2026

*Análisis académico de características de Pokémon legendarios utilizando técnicas fundamentales de análisis exploratorio de datos.*
