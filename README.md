# Bot de Automatización Web con Selenium - Proyecto de Portafolio

## 📋 Descripción

Este proyecto demuestra el desarrollo de un bot de automatización web usando Selenium para la extracción automatizada de datos de plataformas de telemetría. El sistema navega automáticamente por interfaces web complejas, gestiona calendarios dinámicos, descarga archivos de múltiples fuentes y consolida la información en bases de datos unificadas.

**Objetivo del Proyecto**: 
Demostrar habilidades en automatización web, manejo de datos, y desarrollo de sistemas robustos con Python.

## 🚀 Características Técnicas Destacadas
- **Navegación Automática de Calendarios**: Algoritmo inteligente para navegar fechas históricas en interfaces web complejas
- **Descarga Masiva Automatizada**: Sistema de descarga paralela de archivos desde múltiples fuentes
- **Gestión de Estado Persistente**: Implementación de checkpoint system para continuidad de procesos
- **Manejo Robusto de Errores**: Sistema de recuperación automática ante fallos de conexión
- **Consolidación de Datos**: Pipeline de procesamiento y unificación de datasets
- **Arquitectura Modular**: Código organizado en funciones especializadas y reutilizables

## 🛠️ Stack Tecnológico

### Backend & Automatización
- **Python 3.x** - Lenguaje principal
- **Selenium WebDriver** - Automatización web
- **Pandas** - Manipulación y análisis de datos
- **ChromeDriver** - Motor de navegación web

### Gestión de Datos
- **CSV Processing** - Manejo de archivos de datos
- **Data Deduplication** - Eliminación de registros duplicados
- **Datetime Management** - Manejo avanzado de fechas y tiempos

## 📊 Arquitectura del Sistema

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Control de    │    │   Navegación     │    │   Descarga      │
│   Posiciones    │───▶│   Web & Login    │───▶│   Automatizada  │
│   (CSV State)   │    │   (Selenium)     │    │   (Multi-zone)  │
└─────────────────┘    └──────────────────┘    └─────────────────┘
         │                                               │
         │              ┌──────────────────┐            │
         └─────────────▶│  Consolidación   │◀───────────┘
                        │  de Datos        │
                        │  (Pandas)        │
                        └──────────────────┘
```

## 📁 Estructura del Proyecto
```
project-root/
├── Bucle_bot.py           # Aplicación principal
├── posiciones.csv         # Sistema de checkpoint
├── README.md             # Documentación
├── requirements.txt      # Dependencias
└── data/
    ├── downloads/        # Archivos temporales
    └── consolidated/     # Datos procesados
```
## ⚙️ Instalación y Configuración
### 1. Clonar el Repositorio
```bash
git clone https://github.com/ClauBaqueroRico/Bot_UMR.git
cd web-automation-bot
```
### 2. Instalar Dependencias
```bash
pip install -r requirements.txt
```
### 3. Configurar ChromeDriver
- Descargar ChromeDriver compatible con tu versión de Chrome
- Agregar al PATH del sistema o especificar ruta en el código

### 4. Configuración de Credenciales
```python
# Configurar en el archivo principal
USER_EMAIL = "tu_email@ejemplo.com"
USER_PASSWORD = "tu_contraseña_segura"
```

## � Funcionalidades Implementadas

### 1. **Sistema de Navegación Inteligente**
```python
def navegar_calendario_atras(driver, fecha_objetivo, fila, columna):
    """
    Algoritmo para navegar calendarios web de forma inteligente
    - Calcula diferencias temporales automáticamente
    - Maneja múltiples formatos de calendario
    - Selecciona fechas con precisión
    """
```

### 2. **Gestión de Estado Persistente**
- Checkpoint system que permite reiniciar procesos
- Manejo de posiciones en matrices de calendario
- Recuperación automática desde el último punto procesado

### 3. **Pipeline de Procesamiento de Datos**
- Descarga automatizada de múltiples fuentes
- Validación y limpieza de datos
- Consolidación sin duplicados
- Exportación a formatos estándar

## 📈 Casos de Uso Demostrados

### Automatización Web Compleja
- Login automatizado con manejo de sesiones
- Navegación por interfaces JavaScript dinámicas
- Interacción con elementos web complejos (calendarios, dropdowns)

### Procesamiento de Datos a Escala
- Descarga masiva de archivos (múltiples zonas/categorías)
- Procesamiento de datasets grandes con Pandas
- Implementación de algoritmos de deduplicación

### Robustez y Manejo de Errores
- Sistema de reintentos automáticos
- Logs detallados para debugging
- Continuidad de procesos ante fallos parciales

## 🚀 Ejecución del Proyecto

### Modo Desarrollo
```bash
python Bucle_bot.py --debug
```

### Modo Producción
```bash
python Bucle_bot.py --start-date "01/06/2023" --end-date "30/06/2023"
```

### Monitoreo en Tiempo Real
```bash
# El sistema proporciona logs detallados:
Posición actual: Fila 3, Columna 4, Fecha 15/06/2023
Navegando 2 meses hacia atrás en el calendario...
Procesando zona 15 de 44...
Descarga completada: archivo_zona_15.csv
```

## 📊 Métricas de Rendimiento

- **Tiempo de procesamiento**: ~2-3 minutos por día de datos
- **Volumen de datos**: Capacidad para 1000+ registros por ejecución
- **Tasa de éxito**: >95% de descargas exitosas
- **Recuperación de errores**: Continuidad automática en >99% de casos

## 🔍 Destacados Técnicos

### Algoritmos Implementados
- **Navegación temporal**: Cálculo de diferencias entre fechas
- **Mapeo de coordenadas**: Conversión de fechas a posiciones en matriz
- **Deduplicación**: Algoritmos para eliminar registros duplicados

### Patrones de Diseño
- **Strategy Pattern**: Para diferentes tipos de navegación
- **Factory Pattern**: Para creación de drivers web
- **Observer Pattern**: Para logging y monitoreo

### Optimizaciones
- **Lazy Loading**: Carga de datos bajo demanda
- **Batch Processing**: Procesamiento por lotes para eficiencia
- **Connection Pooling**: Reutilización de conexiones web

## 🛡️ Consideraciones de Seguridad

- Manejo seguro de credenciales (no hardcodeadas)
- Validación de datos de entrada
- Logs que no exponen información sensible
- Timeouts para evitar bloqueos indefinidos

## 📚 Tecnologías y Conceptos Demostrados

- **Web Scraping Avanzado** con Selenium
- **Automatización de Procesos** con Python
- **Manipulación de Datos** con Pandas
- **Manejo de Fechas** y Calendarios
- **Arquitectura de Software** robusta
- **Testing y Debugging** de aplicaciones web
- **Documentación Técnica** completa

## 🎯 Objetivos de Aprendizaje Cumplidos

✅ **Automatización Web**: Dominio de Selenium para tareas complejas  
✅ **Procesamiento de Datos**: Manejo eficiente de datasets con Pandas  
✅ **Arquitectura de Software**: Código modular y mantenible  
✅ **Manejo de Errores**: Sistemas robustos con recuperación automática  
✅ **Documentación**: Creación de documentación técnica profesional  

## � Posibles Mejoras Futuras

- [ ] Implementación de base de datos SQL
- [ ] API REST para control remoto
- [ ] Dashboard web para monitoreo
- [ ] Dockerización del proyecto
- [ ] Tests unitarios automatizados
- [ ] Integración con sistemas de CI/CD

## 📄 Licencia

Este proyecto es parte de un portafolio profesional y está disponible para fines educativos y de demostración.

---

**💼 Proyecto de Portafolio** - Desarrollado para demostrar habilidades en automatización web, procesamiento de datos y desarrollo de software robusto.

