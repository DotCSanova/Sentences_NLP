# Análisis de Frases con Procesamiento de Lenguaje Natural (NLP)

## Descripción del Proyecto

Este proyecto implementa un análisis completo de un dataset de 100 frases descriptivas en inglés utilizando técnicas avanzadas de Procesamiento de Lenguaje Natural (NLP). El análisis incluye tanto aspectos estructurales como semánticos, demostrando el uso de modelos de transformers modernos para tareas de comprensión de texto.

**Autor:** Alberto López Casanova  
**Proyecto:** Prueba técnica para Cambrian Intelligence

## Tareas Realizadas

### 1. **Análisis Exploratorio de Datos (EDA)**
- Carga y visualización inicial del dataset
- Análisis estadístico de longitud de frases (palabras y caracteres)
- Visualización de distribuciones mediante histogramas
- Identificación de patrones en la estructura de las frases

### 2. **Análisis Estructural y Gramatical con spaCy**
- Tokenización y análisis de estructura gramatical
- Extracción de etiquetas POS (Part-of-Speech) y dependencias sintácticas
- Creación de matriz de similitud estructural entre frases
- Identificación de frases únicas o outliers estructurales
- Clustering basado en similitud gramatical

### 3. **Análisis Semántico con Sentence-BERT (SBERT)**
- Generación de embeddings semánticos usando el modelo `all-MiniLM-L6-v2`
- Creación de matriz de similitud semántica mediante distancia coseno
- Clustering semántico de frases usando Agglomerative Clustering
- Identificación de grupos temáticos basados en significado

### 4. **Caso de Uso: Búsqueda Semántica**
- Implementación de sistema de búsqueda semántica
- Búsqueda de frases más similares a una consulta dada
- Demostración práctica con consultas de ejemplo

## Tecnologías Utilizadas

- **Python 3.10+**
- **spaCy** - Análisis gramatical y estructural
- **Sentence Transformers** - Generación de embeddings semánticos
- **scikit-learn** - Clustering y análisis de similitud
- **pandas & numpy** - Manipulación y análisis de datos
- **matplotlib & seaborn** - Visualización de datos
- **torch** - Pytorch

## Instalación

### Prerrequisitos
- Python 3.10 o superior
- [uv](https://docs.astral.sh/uv/) (gestor de paquetes Python)

### Pasos de Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone <url-del-repositorio>
   cd Sentences_NLP
   ```

2. **Crear entorno virtual e instalar dependencias con uv:**
   ```bash
   uv sync
   ```

3. **Descargar modelo de spaCy:**
   ```bash
   uv run -- spacy download en_core_web_trf
   ```

## Uso

### Ejecutar el Notebook
```bash
uv run --with jupyter jupyter lab
```

### Estructura de Archivos
```
Sentences_NLP/
├── sentences_NLP.ipynb    # Notebook principal con el análisis
├── sentences.json         # Dataset de 100 frases descriptivas
├── pyproject.toml        # Configuración del proyecto
├── README.md            # Este archivo
└── uv.lock             # Archivo de bloqueo de dependencias
```

## Resultados Principales

### Análisis Estructural
- **Longitud promedio:** 11.49 palabras por frase
- **Distribución:** Normal con desviación estándar de 2.02 palabras
- **Patrón común:** Frases descriptivas que comienzan con "The"

### Análisis Semántico
- **13 clusters** identificados basados en similitud semántica
- **Grupos temáticos** incluyen: naturaleza, animales, plantas, objetos culturales
- **Búsqueda semántica** efectiva para encontrar frases relacionadas

### Casos de Uso Demostrados
1. **Clustering semántico** de frases por significado
2. **Búsqueda semántica** para encontrar frases similares
3. **Análisis de outliers** estructurales y semánticos

## 🔧 Configuración del Entorno

El proyecto utiliza `uv` como gestor de paquetes, que ofrece:
- **Instalación rápida** de dependencias
- **Resolución de conflictos** automática
- **Entornos virtuales** integrados
- **Compatibilidad** con pip y conda

### Comandos útiles de uv:
```bash
# Instalar dependencias
uv add [dependencia]

# Ejecutar script
uv run .\main.py  

# Activar entorno virtual
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows
```

## Características Destacadas

- **Análisis NLP:** Combina análisis estructural y semántico
- **Modelos modernos:** Utiliza transformers para embeddings semánticos
- **Visualización completa:** Gráficos para análisis
- **Código reproducible:** Notebook estructurado con explicaciones detalladas
- **Gestión de dependencias:** Configuración optimizada con uv

## Licencia

Este proyecto es parte de una prueba técnica para Cambrian Intelligence.

---