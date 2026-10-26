# Radar_permanencia_estudiantil

 ## 🎯 Objetivo 
Este proyecto lo hice para aprender análisis predictivo. Construí un modelo de regresión logística para estimar el riesgo de abandono, lo evalué con ROC-AUC y PR-AUC.  Sirve para priorizar a quién apoyar, no para asegurar quién abandonará.

Pregunta a responder: 
¿A qué estudiantes podemos contactar?
¿En qué semestre estan?
¿Qué variables pueden estar influyendo en la deserción estudiantil?


Dataset: academic_survival_longitudinal.csv (Kaggle: Student Retention & Academic Performance Data).
Link a la fuente original : https://www.kaggle.com/datasets/razanihababdellatif/student-retention-and-academic-performance-data

## 🛠️ Herramientas Utilizadas
Stack: Python (Jupyter) para limpieza, EDA y modelo → Power BI para análisis y visualización.

## KPIs monitoreados
Total de Estudiantes <br>
Estudiantes Inscritos - hoy <br>
Estudiantes que Abandonaron   <br>
Estudiantes Graduados    <br>
% Abandono acumulado  <br>
% Alumgnos Graduados    <br>
% Tasa de abandono por semestre  <br>

## Proceso realizado
- Conexión y Exploración de los Datos 
- Limpieza y transformación de datos
- Validación de Calidad
- Modelo: regresión logística -  probabilidad de abandono
- Generación de archivo CVS con alumnos con indicador de probabilidad de riesgo de abandono
- Carga de datos en POWER BI
- Creación de métricas en DAX
- Diseño y planificación
- Generación de insights para toma de decisiones
- Narrativa del Dashboard 

Principales insights:
1. El modelo ordena a los estudiantes por riesgo con una capacidad discriminativa buena (ROC-AUC 0.80) y rinde casi cuatro veces mejor que el azar para encontrar a quienes abandonan (PR-AUC 0.39 frente a 0.10). Sirve para priorizar a quién contactar, no para predecir con certeza el caso individual. Los niveles de riesgo del modelo sí separan a quienes abandonan: en el grupo alto abandona casi 3 de cada 10 y en el bajo, 3 de cada 100.

<img width="311" height="303" alt="chart1" src="https://github.com/user-attachments/assets/ff920684-30f7-4cca-a29f-5dfa84b838a5" />
Los factores que más se asocian con el abandono son los cursos reprobados, el estrés financiero y ser de primera generación; el GPA alto y la beca se asocian con menos riesgo.
<img width="434" height="310" alt="Char3" src="https://github.com/user-attachments/assets/dfa4c6b8-b728-4725-9559-5882c5be8daf" />

Limitaciones El modelo estima riesgo, no causalidad, y no predice con certeza el caso individual Los resultados corresponden a un conjunto de prueba con estudiantes que el modelo no vio.

