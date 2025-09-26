# 🏠 Finca Raíz Ibagué - Web Scraping y Predicción

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 Descripción

Este proyecto implementa un sistema de **web scraping** y **análisis predictivo** para el mercado inmobiliario de apartamentos en arriendo en Ibagué, Colombia. Utiliza técnicas de extracción automatizada de datos de portales inmobiliarios y modelos de machine learning para predecir precios de arriendo.

### 🎯 Objetivos

- **Extracción automatizada** de datos de propiedades en arriendo.
- **Análisis exploratorio** del mercado inmobiliario local.
- **Modelado predictivo** de precios de arriendo.

### 📊 Estructura del Proyecto

Los notebooks están organizados secuencialmente para facilitar la ejecución:

- **`01_WSFincaRaizIbague.ipynb`** → Web scraping y obtención de datos.
- **`02_PrediccionFincaRaizIbague.ipynb`** → Procesamiento, modelado y visualización.

Archivos generados (según la fecha en formato YYYYMMDD) aparecen en la carpeta __Datos__:
- YYYYMMDD_enlaces_apartamentos.parquet
- YYYYMMDD_apartamentos_ibague.parquet

## 🚀 Instalación y Configuración

### Prerrequisitos

- Python 3.7 o superior
- pip (gestor de paquetes de Python)
- Git (para clonar el repositorio)

### 🔧 Instalación

1. **Clonar el repositorio:**
```bash
git clone https://github.com/fcochaux/finca-raiz-ibague-scraping-prediccion.git
cd finca-raiz-ibague-scraping-prediccion
```

2. **Crear y activar entorno virtual:**
```bash
# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate

# Windows
python -m venv .venv
.venv\Scripts\activate
```

3. **Instalar dependencias:**
```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

5. **Iniciar Jupyter:**
```bash
jupyter lab
# o
jupyter notebook
```

## 📖 Uso

### Orden de Ejecución

1. **Web Scraping**: Ejecuta `01_WSFincaRaizIbague.ipynb` para extraer datos
2. **Análisis y Predicción**: Ejecuta `02_PrediccionFincaRaizIbague.ipynb` para procesar y modelar

### 📁 Estructura de Archivos

```
finca-raiz-ibague-scraping-prediccion/
├── datos/                                     # Carpeta de datos organizados
│   ├── 20250918_enlaces_apartamentos.parquet  # Enlaces de propiedades
│   └── 20250918_apartamentos_ibague.parquet   # Datos completos de propiedades
├── 01_WSFincaRaizIbague.ipynb                 # Web scraping automatizado
├── 02_PrediccionFincaRaizIbague.ipynb         # ML pipeline avanzado
├── requirements.txt                           # Dependencias del proyecto
├── README.md                                  # Documentación
└── LICENSE                                    # Licencia MIT
```

### 📊 Datos Generados

Los datos se organizan automáticamente con formato de fecha:
- **`YYYYMMDD_enlaces_apartamentos.parquet`** - URLs de propiedades extraídas
- **`YYYYMMDD_apartamentos_ibague.parquet`** - Dataset completo con características de propiedades

## 🛠️ Tecnologías Utilizadas

### Web Scraping y Procesamiento
- **Python 3.x** - Lenguaje principal
- **Pandas** - Manipulación y análisis de datos
- **Requests** - Web scraping HTTP
- **LXML** - Parsing HTML eficiente
- **NumPy** - Computación numérica

### Machine Learning y Análisis
- **Scikit-learn** - Algoritmos de ML y preprocesamiento
- **GridSearchCV** - Optimización de hiperparámetros
- **Pipeline** - Automatización de flujos de trabajo
- **Cross-validation** - Validación robusta de modelos

### Visualización
- **Matplotlib** - Visualizaciones estáticas
- **Seaborn** - Gráficos estadísticos avanzados

### Desarrollo
- **Jupyter Notebooks** - Desarrollo interactivo y documentación

## 📊 Características Avanzadas

### 🔍 Web Scraping Inteligente
- ✅ **Extracción automatizada** de datos inmobiliarios desde Finca Raíz
- ✅ **Detección automática** de archivos más recientes
- ✅ **Manejo robusto** de errores y excepciones
- ✅ **Estructura organizada** de datos en carpeta dedicada

### 📈 Análisis de Datos Profesional
- ✅ **Análisis exploratorio completo (EDA)** con visualizaciones
- ✅ **Ingeniería de características** avanzada
- ✅ **Limpieza y preprocesamiento** automatizado
- ✅ **Identificación y tratamiento** de datos atípicos
- ✅ **Imputación inteligente** de valores faltantes

### 🤖 Machine Learning Avanzado
- ✅ **Pipeline automatizado** con Scikit-learn
- ✅ **Múltiples algoritmos**: LinearRegression, Ridge, RandomForest, SVR
- ✅ **GridSearchCV** para optimización de hiperparámetros
- ✅ **Validación cruzada** de 5 particiones
- ✅ **Comparación sistemática** de modelos
- ✅ **Métricas robustas** de evaluación (RMSE, MAE, R²)

### 📊 Visualización
- ✅ **Visualizaciones interactivas** con Seaborn y Matplotlib
- ✅ **Análisis de distribución** de precios por zonas
- ✅ **Gráficos estadísticos** avanzados

## 📊 Resultados del Modelamiento

### Algoritmos Implementados
El pipeline de machine learning incluye los siguientes algoritmos con optimización automática y preprocesamiento uniforme (StandardScaler):

| Algoritmo          | Características                         | Optimización |
|--------------------|------------------------------------------|--------------|
| **LinearRegression** | Regresión lineal básica                  | Sin hiperparámetros |
| **Ridge**            | Regresión con regularización L2          | Alpha: [0.01, 0.1, 1.0, 10.0] |
| **Lasso**            | Regresión con regularización L1          | Alpha: [0.01, 0.1, 1.0, 10.0] |
| **RandomForest**     | Ensemble de árboles de decisión          | n_estimators: [50, 100], max_depth: [5, 10, None] |
| **SVR**              | Support Vector Regression               | C: [0.1, 1, 10], kernel: [linear, rbf] |
| **GradientBoosting** | Gradient Boosting Regressor             | learning_rate: [0.05, 0.1], n_estimators: [50, 100], max_depth: [3, 5] |

### Transformación de la Variable Objetivo
Para mejorar la estabilidad del modelo y reducir la influencia de valores extremos, la variable objetivo (precio) se transformó mediante logaritmo natural.  
Esto permite interpretar los errores en términos relativos y mejora la capacidad de generalización de los modelos.

### Métricas de Evaluación
- **RMSE** (Root Mean Square Error) – Error cuadrático medio en escala log
- **MAE** (Mean Absolute Error) – Error absoluto medio en escala log
- **R²** (Coefficient of Determination) – Proporción de variabilidad explicada
- **Validación cruzada** de 5 particiones para una evaluación robusta

### Proceso de Optimización
- **GridSearchCV** para búsqueda exhaustiva de hiperparámetros
- **Pipeline automatizado** con preprocesamiento integrado
- **Comparación sistemática** de rendimiento entre modelos
- **Selección del modelo más prometedor** según las métricas en el conjunto de prueba

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👨‍💻 Autor

**Francisco José Chaux Guzmán** - [@fcochaux](https://github.com/fcochaux)

## 📈 Roadmap

### ✅ Completado
- [x] **Web scraping automatizado** desde Finca Raíz
- [x] **Pipeline de ML avanzado** con múltiples algoritmos
- [x] **Optimización de hiperparámetros** con GridSearchCV
- [x] **Validación cruzada** robusta
- [x] **Organización de datos** en estructura profesional
- [x] **Análisis exploratorio completo** (EDA)
- [x] **Ingeniería de características** avanzada

### 🚀 En Desarrollo
- [ ] **Dashboard interactivo** con Streamlit/Dash
- [ ] **API REST** para consultas en tiempo real
- [ ] **Análisis de tendencias temporales**
- [ ] **Integración con más fuentes** de datos inmobiliarios

### 🔮 Futuro
- [ ] **Modelos de deep learning** (Neural Networks)
- [ ] **Predicción de tendencias** del mercado
- [ ] **Análisis de sentimientos** de descripciones
- [ ] **Recomendador de propiedades** personalizado
