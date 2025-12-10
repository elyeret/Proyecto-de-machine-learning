
# Proyecto-de-machine-learning


## Repositorio: Análisis de Expresión Génica para Diagnóstico de Parkinson con Machine Learning

En este repositorio se le añadirá un trabajo final del curso de machine learning




## Descripción del Proyecto
Este repositorio contiene un flujo de trabajo completo para el análisis de datos de expresión génica aplicado al diagnóstico de la enfermedad de Parkinson mediante técnicas de Machine Learning. El proyecto integra procesamiento de datos, modelado predictivo y explicabilidad de modelos, proporcionando una herramienta transparente y reproducible para investigación en biomedicina.

# Estructura de Archivos y Contenido
1. Datos y Metadatos
meta_data_PD_RNA_UPDRS3BUV08wo... → Metadatos de pacientes con Parkinson, incluyendo información clínica y posiblemente puntuaciones UPDRS3 (escala de evaluación motora).

Estadísticas. Completas.xlsx → Estadísticas descriptivas completas del conjunto de datos (expresión génica, características clínicas, etc.).

valores_atipicos_zscore.xlsx & valores_atipicos_zscore_jqr.xlsx → Identificación de valores atípicos utilizando métodos Z-score y Rango Intercuartílico (IQR), esencial para limpieza de datos.

2. Modelado y Resultados
importancias_random_forest.xlsx → Ranking de importancia de variables (genes) obtenido del modelo Random Forest.

output.png → Gráfico de valores SHAP que explica el impacto de cada gen en las predicciones del modelo, permitiendo interpretación biológica.

README.md → Documentación principal del repositorio (instrucciones, metodología, referencias).

3. Código y Procesamiento
Untitled1.ipynb → Notebook de Jupyter con el código ejecutable que contiene:

Carga y preprocesamiento de datos

Implementación del modelo Random Forest

Generación de curvas ROC y cálculo de AUC

Análisis SHAP para explicabilidad

Visualización de resultados (top 10 genes, curva ROC, gráficos SHAP)

## Metodología y Hallazgos Clave
# Selección de Genes Biomarcadores
Se identificaron los 10 genes más influyentes en el diagnóstico:

ENSG00000238713

ENSG00000196420

ENSG00000261220

ENSG00000235445

ENSG00000119950

ENSG00000001084

ENSG00000239437

ENSG00000263786

ENSG00000125864

ENSG00000111364

# Rendimiento del Modelo
Modelo utilizado: Random Forest

Métrica de evaluación: Curva ROC con AUC = 0.805

Interpretación: Capacidad predictiva muy buena, superior al azar (0.5) y cercana a excelente (>0.8).

# Explicabilidad (XAI - Explainable AI)
Mediante SHAP se visualiza:

Impacto direccional de cada gen (positivo → Parkinson, negativo → No Parkinson).

Relación expresión-efecto (alto vs. bajo nivel de expresión génica).

20 genes principales analizados en profundidad.

# Tecnologías Utilizadas
Python (pandas, numpy, scikit-learn, shap, matplotlib, seaborn)

Jupyter Notebook para análisis interactivo

Excel para revisión manual y reportes intermedios

Git/GitHub para control de versiones

# Objetivos del Repositorio
Reproducibilidad: Ofrecer un flujo de trabajo claro y documentado.

Transparencia: Explicar no solo el "qué" sino el "por qué" de las predicciones.

Investigación traslacional: Conectar hallazgos bioinformáticos con aplicaciones clínicas potenciales.

Educación: Servir como ejemplo de aplicación de ML en biomedicina con explicabilidad.


# Cómo Usar Este Repositorio
Clonar el repositorio.


Ejecutar Untitled1.ipynb paso a paso (preferiblemente en un entorno virtual).

Consultar los archivos Excel para datos crudos y resultados intermedios.

Revisar las imágenes generadas (output.png, gráficos ROC) para interpretación visual.

# Posibles Extensiones Futuras
Integración con datos de imágenes médicas o secuenciación completa.

Implementación de otros modelos (XGBoost, redes neuronales).

Validación externa con cohortes independientes.

Desarrollo de una interfaz web para uso clínico simplificado.


