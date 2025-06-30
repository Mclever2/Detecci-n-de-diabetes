# Sistema de Detección de Diabetes con Inteligencia Artificial

## Descripción del Proyecto

Este proyecto implementa un **sistema de detección temprana de diabetes** utilizando técnicas avanzadas de **Machine Learning** y **Inteligencia Artificial**. El sistema analiza múltiples factores de riesgo y biomarcadores clínicos para predecir la probabilidad de que una persona desarrolle diabetes.

## Objetivo

El objetivo principal es proporcionar una herramienta de **screening médico** que permita identificar individuos en riesgo de diabetes de manera rápida y no invasiva, facilitando la detección temprana y la intervención médica oportuna.

## Arquitectura del Sistema

### Componentes Principales

1. **Módulo de Análisis de Datos**: Procesamiento y limpieza de datasets médicos
2. **Motor de Machine Learning**: Algoritmo Random Forest entrenado
3. **Interfaz Web Interactiva**: Aplicación web para entrada de datos y resultados
4. **Sistema de Predicción**: Generación de probabilidades y recomendaciones

## Datasets Utilizados

### Dataset Principal (diabetes_prediction_dataset.csv)
- **100,000 registros** de pacientes
- **9 variables** clínicas y demográficas
- **Distribución balanceada** de casos positivos y negativos

### Variables de Entrada

#### Datos Demográficos
- **Género**: Factor de riesgo demográfico
- **Edad**: Variable continua (0.08 - 80 años)

#### Historial Médico
- **Hipertensión**: Condición médica preexistente (0/1)
- **Enfermedad Cardíaca**: Factor de riesgo cardiovascular (0/1)
- **Historial de Tabaquismo**: Categorizado en 6 niveles

#### Biomarcadores Clínicos
- **IMC (Índice de Masa Corporal)**: 10.01 - 95.69
- **HbA1c (Hemoglobina Glicosilada)**: 3.5% - 9.0%
- **Nivel de Glucosa en Sangre**: 80 - 300 mg/dL

## Algoritmo de Machine Learning

### Random Forest Classifier
- **Tipo**: Ensemble Learning (Bosque Aleatorio)
- **Ventajas**: 
  - Alta precisión en datos médicos
  - Manejo robusto de variables mixtas
  - Resistente al overfitting
  - Interpretabilidad de características importantes

### Proceso de Entrenamiento
1. **División Estratificada**: 70% entrenamiento, 20% prueba, 10% validación
2. **Preprocesamiento**: Codificación de variables categóricas
3. **Optimización**: Ajuste de hiperparámetros
4. **Validación Cruzada**: Múltiples iteraciones de validación

## Métricas de Rendimiento

### Resultados del Modelo
- **Accuracy (Precisión Global)**: 97.13%
- **Precision (Precisión)**: 92.24%
- **Recall (Sensibilidad)**: 58.42%
- **F1-Score**: 71.53%

### Interpretación
- **Alta precisión**: El modelo raramente da falsos positivos
- **Sensibilidad moderada**: Detecta correctamente la mayoría de casos positivos
- **Balance general**: Buen equilibrio entre precisión y sensibilidad

## Interfaz de Usuario

### Características de la Aplicación Web
- **Framework**: Gradio (interfaz moderna y responsiva)
- **Diseño**: Interfaz intuitiva con controles deslizantes y botones
- **Validación**: Verificación automática de rangos de datos
- **Resultados Visuales**: Presentación clara con códigos de color

### Flujo de Usuario
1. **Entrada de Datos**: Formulario interactivo con validación
2. **Procesamiento**: Análisis en tiempo real por el modelo IA
3. **Resultado**: Predicción con porcentaje de riesgo
4. **Recomendaciones**: Consejos personalizados según el resultado

## Presentación de Resultados

### Códigos de Color
- **Verde**: Bajo riesgo de diabetes
- **Rojo**: Alto riesgo de diabetes

### Información Proporcionada
- **Porcentaje de Riesgo**: Probabilidad calculada por el modelo
- **Recomendaciones Médicas**: Consejos específicos según el resultado
- **Advertencias**: Recordatorios sobre consulta médica profesional

## Análisis de Datos

### Exploración Inicial
- **Calidad de Datos**: Verificación de valores nulos y duplicados
- **Distribuciones**: Análisis de la distribución de variables
- **Correlaciones**: Identificación de relaciones entre variables
- **Outliers**: Detección y manejo de valores atípicos

### Preprocesamiento
- **Limpieza**: Eliminación de duplicados (3,854 registros removidos)
- **Codificación**: Transformación de variables categóricas
- **Normalización**: Ajuste de escalas para variables numéricas

## Características del Modelo

### Ventajas del Random Forest
- **Robustez**: Manejo efectivo de ruido en datos médicos
- **Interpretabilidad**: Identificación de variables más importantes
- **Generalización**: Buen rendimiento en datos no vistos
- **Estabilidad**: Resultados consistentes entre ejecuciones

### Variables Más Importantes
1. **Nivel de Glucosa en Sangre**: Biomarcador principal
2. **HbA1c**: Indicador de control glucémico a largo plazo
3. **IMC**: Factor de riesgo metabólico
4. **Edad**: Factor demográfico significativo

## Casos de Uso

### Aplicaciones Principales
- **Screening Preventivo**: Identificación temprana de riesgo
- **Monitoreo de Pacientes**: Seguimiento de factores de riesgo
- **Educación Médica**: Herramienta de concientización
- **Investigación**: Análisis de patrones epidemiológicos

### Población Objetivo
- **Adultos**: 18-80 años
- **Pacientes Asintomáticos**: Sin diagnóstico previo
- **Grupos de Riesgo**: Con factores predisponentes

## Limitaciones y Consideraciones

### Limitaciones del Modelo
- **No es Diagnóstico**: Herramienta de screening, no reemplaza evaluación médica
- **Datos Históricos**: Basado en patrones de datos existentes
- **Variables Limitadas**: No incluye todos los factores de riesgo conocidos

### Consideraciones Éticas
- **Privacidad**: Protección de datos personales
- **Responsabilidad**: Uso apropiado de herramientas de IA
- **Transparencia**: Explicación clara de limitaciones

## Tecnologías Utilizadas

### Stack Tecnológico
- **Python**: Lenguaje principal de programación
- **Pandas**: Manipulación y análisis de datos
- **Scikit-learn**: Algoritmos de machine learning
- **Matplotlib/Seaborn**: Visualización de datos
- **Gradio**: Interfaz web interactiva
- **NumPy**: Computación numérica

### Librerías Especializadas
- **Joblib**: Serialización del modelo entrenado
- **Scikit-learn**: Métricas de evaluación y validación
- **Gradio**: Framework para aplicaciones web de IA

## Distribución de Datos

### Características del Dataset
- **Total de Registros**: 100,000 pacientes
- **Casos Positivos**: 8,500 (8.5%)
- **Casos Negativos**: 91,500 (91.5%)
- **Variables**: 9 características clínicas

### Balance de Clases
- **Desbalance Moderado**: Típico en datos médicos
- **Estrategia**: División estratificada para mantener proporciones
- **Validación**: Múltiples métricas para evaluación completa

Este sistema representa una aplicación práctica de **Inteligencia Artificial en el campo de la salud**, demostrando cómo las técnicas de machine learning pueden contribuir a la **medicina preventiva** y la **detección temprana de enfermedades**.