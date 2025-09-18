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

### 📁 Archivos Generados

Los datos extraídos se guardan con formato de fecha:
- `YYYYMMDD_enlaces_apartamentos.csv` - Enlaces de propiedades
- `YYYYMMDD_apartamentos_ibague.csv` - Datos completos de propiedades

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Pandas** - Manipulación de datos
- **Requests** - Web scraping
- **LXML** - Parsing HTML
- **Folium** - Visualización de mapas
- **Jupyter Notebooks** - Desarrollo interactivo

## 📊 Características

- ✅ Extracción automatizada de datos inmobiliarios
- ✅ Limpieza y procesamiento de datos
- ✅ Análisis exploratorio de datos (EDA)
- ✅ Modelado predictivo de precios
- ✅ Visualizaciones interactivas
- ✅ Mapas georreferenciados

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

- [ ] Implementar más fuentes de datos
- [ ] Mejorar modelos predictivos
- [ ] Dashboard interactivo
- [ ] API REST para consultas
- [ ] Análisis de tendencias temporales
