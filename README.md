# Radar de Permanencia Estudiantil

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

<img width="291" height="283" alt="chart1" src="https://github.com/user-attachments/assets/ff920684-30f7-4cca-a29f-5dfa84b838a5" />

Los factores que más se asocian con el abandono son los cursos reprobados, el estrés financiero y ser de primera generación; el GPA alto y la beca se asocian con menos riesgo.

<img width="414" height="290" alt="Char3" src="https://github.com/user-attachments/assets/dfa4c6b8-b728-4725-9559-5882c5be8daf" />

Limitaciones El modelo estima riesgo, no causalidad, y no predice con certeza el caso individual. 

2. Los resultados del modelo nos arrojan que:
- El 7o. semestre concentra el mayor riesgo  con un 14.7%, casi el doble que el segundo semestre.
- Solo el 7% de los alumnos se graduan.
- La tasa de abandono por semestre es de a un 10.2%, es decir 2040 alumnos.
 <img width="780" height="458" alt="PB1" src="https://github.com/user-attachments/assets/1ddb5413-9ecb-438e-b6f6-55e93569f90b" />
 
 3. Dentro de los factors asociados al abandono encontramos que:
- Destaca el número de cursos no aprobados. El riesgo se multiplica por 14, pasando de 5.3% si no tiene cursos reprobados a un 72.2% con  5 cursos no aprobados.
- Los alumnos sin beca tienen un porcentaje 3.9 puntos mayor que los alumnos con beca. De 11.
  
  <img width="782" height="449" alt="PBI2" src="https://github.com/user-attachments/assets/5e8ec425-10e8-4c9a-9e2c-7a419cf5af5c" />
  
4. El modelo es útil para priorizar, no para predecir con certeza. Los alumnos clasificados como riesgo alto abandonan casi 10 veces más que los de riesgo bajo (29.6 % vs. 3.1 %), por lo que concentrar los recursos de acompañamiento en ellos es más eficiente que atender a todos por igual. Sin embargo, 7 de cada 10 alumnos de riesgo alto no abandonan, por lo que el modelo debe usarse como una herramienta de alerta temprana y no como un diagnóstico individual.
   
<img width="655" height="370" alt="PBI3" src="https://github.com/user-attachments/assets/969f90dc-e627-4331-8d0b-f219b6b2504b" />




