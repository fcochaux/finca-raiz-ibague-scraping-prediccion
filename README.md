# 🏠 Finca Raíz Ibagué - Web Scraping y Predicción

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 Descripción

Este proyecto implementa un sistema completo de **web scraping** y **análisis predictivo** para el mercado inmobiliario de apartamentos en arriendo en Ibagué, Colombia. Utiliza técnicas de extracción automatizada de datos de portales inmobiliarios y modelos de machine learning para predecir precios de arriendo.

### 🎯 Objetivos

- **Extracción automatizada** de datos de propiedades en arriendo
- **Análisis exploratorio** del mercado inmobiliario local
- **Modelado predictivo** de precios de arriendo
- **Visualización interactiva** de resultados

### 📊 Estructura del Proyecto

Los notebooks están organizados secuencialmente para facilitar la ejecución:

- **`01_WSFincaRaizIbague.ipynb`** → Web scraping y obtención de datos
- **`02_PrediccionFincaRaizIbague.ipynb`** → Procesamiento, modelado y visualización

Archivos CSV generados (según la fecha en formato YYYYMMDD):
- YYYYMMDD_enlaces_apartamentos.csv
- YYYYMMDD_apartamentos_ibague.csv

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

4. **Verificar instalación:**
```bash
python -c "import folium; print('✅ folium OK', folium.__version__)"
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
├── datos/                                    # Carpeta de datos organizados
│   ├── 20250918_enlaces_apartamentos.csv    # Enlaces de propiedades
│   └── 20250918_apartamentos_ibague.csv     # Datos completos de propiedades
├── 01_WSFincaRaizIbague.ipynb               # Web scraping automatizado
├── 02_PrediccionFincaRaizIbague.ipynb       # ML pipeline avanzado
├── requirements.txt                          # Dependencias del proyecto
├── README.md                                 # Documentación
└── LICENSE                                   # Licencia MIT
```

### 📊 Datos Generados

Los datos se organizan automáticamente con formato de fecha:
- **`YYYYMMDD_enlaces_apartamentos.csv`** - URLs de propiedades extraídas
- **`YYYYMMDD_apartamentos_ibague.csv`** - Dataset completo con características de propiedades

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
- **Folium** - Mapas interactivos georreferenciados

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

### 📊 Visualización y Mapas
- ✅ **Visualizaciones interactivas** con Seaborn y Matplotlib
- ✅ **Mapas georreferenciados** con Folium
- ✅ **Análisis de distribución** de precios por zonas
- ✅ **Gráficos estadísticos** avanzados

## 📊 Resultados del Modelamiento

### Algoritmos Implementados
El pipeline de machine learning incluye los siguientes algoritmos con optimización automática:

| Algoritmo | Características | Optimización |
|-----------|----------------|--------------|
| **LinearRegression** | Regresión lineal básica | StandardScaler |
| **Ridge** | Regresión con regularización L2 | Alpha: [0.1, 1.0, 10.0] |
| **RandomForest** | Ensemble de árboles de decisión | n_estimators: [50, 100], max_depth: [5, 10, None] |
| **SVR** | Support Vector Regression | C: [0.1, 1, 10], kernel: [linear, rbf] |

### Métricas de Evaluación
- **RMSE** (Root Mean Square Error) - Error cuadrático medio
- **MAE** (Mean Absolute Error) - Error absoluto medio  
- **R²** (Coefficient of Determination) - Coeficiente de determinación
- **Validación cruzada** de 5 particiones para evaluación robusta

### Proceso de Optimización
- **GridSearchCV** para búsqueda exhaustiva de hiperparámetros
- **Pipeline automatizado** con preprocesamiento integrado
- **Comparación sistemática** de rendimiento entre modelos
- **Selección automática** del mejor modelo basado en métricas

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para contribuir:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👨‍💻 Autor

**Francisco Chaux** - [@fcochaux](https://github.com/fcochaux)

## ⚠️ Notas Importantes

- **Uso responsable**: Este proyecto es para fines académicos y de investigación
- **Respeto a robots.txt**: Asegúrate de cumplir con las políticas del sitio web
- **Datos actuales**: Los resultados pueden variar según la disponibilidad de datos
- **Entorno virtual**: Siempre usa un entorno virtual para evitar conflictos de dependencias

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
