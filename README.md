# IRIS SPECIES CLASSIFICATION PROJECT 

## Descripción del Proyecto

Este es el **proyecto final** de la asignatura **Data Mining** de la Universidad de la Costa.

El objetivo es desarrollar un **modelo de clasificación de machine learning** capaz de predecir la especie de una flor Iris basándose en cuatro mediciones de características botánicas: largo y ancho de sépalos, largo y ancho de pétalos.

### Dataset
- **Fuente**: UCI Machine Learning Repository (Kaggle)
- **Muestras**: 150 flores
- **Clases**: 3 especies (Iris setosa, Iris versicolor, Iris virginica)
- **Features**: 4 características numéricas

---

## Metodología - Pipeline de Data Mining

### 1.  Data Understanding
- Análisis exploratorio del dataset (EDA)
- Identificación de valores faltantes y duplicados
- Estadísticas descriptivas y distribuciones
- Visualización de correlaciones entre features

### 2.  Data Preprocessing
- Estandarización de features (StandardScaler)
- Eliminación de duplicados
- Separación de variables independientes y dependientes
- Validación de integridad de datos

### 3.  Train-Test Split
- División 80% entrenamiento - 20% prueba
- Estratificación para mantener balance de clases
- Random state fijo para reproducibilidad (seed=42)

### 4.  Modelo: Random Forest Classifier
**Justificación de la selección:**
-  Excelente rendimiento en clasificación multi-clase
-  Manejo robusto de características numéricas
-  Resistencia a outliers y overfitting
-  Proporciona importancia de features
-  No requiere ajuste extensivo de hiperparámetros

**Configuración:**
- Número de árboles: 100
- Criterio de división: Gini
- Max depth: Sin límite (auto)
- Random state: 42

### 5.  Evaluación del Modelo
Métricas calculadas en el conjunto de prueba:
- **Accuracy**: Proporción de predicciones correctas
- **Precision**: TP / (TP + FP) - Precisión por clase
- **Recall**: TP / (TP + FN) - Cobertura por clase
- **F1-Score**: Media armónica entre Precision y Recall
- **Cross-validation**: Validación cruzada 5-fold

---

##  Estructura del Repositorio

```
Mineria-de-datos/
├── project.py                 # Script principal ejecutable
├── requirements.txt           # Dependencias del proyecto
├── README.md                  # Este archivo (documentación)
└── notebooks/
    └── iris_analysis.ipynb    # Notebook de análisis (opcional)
```

---

##  Instalación y Uso

### Requisitos Previos
- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Conexión a internet (para descargar dataset de Kaggle)

### Instalación Local

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Jerzygroxx/Mineria-de-datos.git
   cd Mineria-de-datos
   ```

2. **Crear entorno virtual (recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ejecutar el proyecto:**
   ```bash
   python project.py
   ```


## Resultados Obtenidos

| Métrica | Conjunto de Prueba |
|---------|-------------------|
| **Accuracy** | 96-98% |
| **Precision (weighted)** | 96-98% |
| **Recall (weighted)** | 96-98% |
| **F1-Score (weighted)** | 96-98% |
| **Cross-validation (5-fold)** | 95-97% |

### Interpretación
El modelo demuestra un **excelente desempeño** en la clasificación de especies de Iris, con tasas de acierto superiores al 96%. La validación cruzada confirma la estabilidad del modelo y ausencia de overfitting significativo.

---

## Visualizaciones Generadas

El proyecto genera múltiples visualizaciones interactivas (Plotly):

1. **Matriz de Confusión**: Muestra el desempeño por clase
2. **Importancia de Features**: Ranking de características más influyentes
3. **Distribución de Features**: Histogramas por especie
4. **Matriz de Scatter Plots**: Relaciones entre pares de features
5. **Gráfico 3D**: Visualización tridimensional del dataset

---

## Predicción Interactiva

El modelo permite hacer predicciones personalizadas ingresando valores de:
- Sepal Length (cm)
- Sepal Width (cm)
- Petal Length (cm)
- Petal Width (cm)

---

## Dependencias Principales

| Paquete | Versión | Propósito |
|---------|---------|----------|
| pandas | ≥1.3.0 | Manipulación de datos |
| scikit-learn | ≥1.0.0 | Machine Learning |
| numpy | ≥1.21.0 | Computación numérica |
| plotly | ≥5.0.0 | Visualizaciones interactivas |
| matplotlib | ≥3.4.0 | Gráficos estáticos |
| seaborn | ≥0.11.0 | Visualizaciones estadísticas |
| kagglehub | ≥0.2.0 | Descarga de datasets |

---

##Integrante del Equipo

- **Jorge Perez** - Estudiante

---

## Profesor

**José Escorcia-Gutierrez, Ph.D.**
Departamento de Ciencia de la Computación y Electrónica
Universidad de la Costa

---

## Licencia

Este proyecto es de propósito educativo y es parte del programa académico de la Universidad de la Costa.

---

## Contacto y Soporte

Si tienes preguntas sobre el proyecto o encontraste un error, por favor abre un **issue** en GitHub.

---

##  Conclusiones

Este proyecto demuestra la aplicación práctica del pipeline completo de Data Mining:
-  Comprensión profunda de los datos
-  Preparación y limpieza rigurosa
-  Selección justificada de modelos
-  Evaluación exhaustiva del desempeño
-  Comunicación clara de resultados

El modelo de Random Forest proporciona una solución robusta y confiable para la clasificación de especies de Iris.

---

**Última actualización**: Noviembre 2024
**Estado del Proyecto**:  Completado y Validado
