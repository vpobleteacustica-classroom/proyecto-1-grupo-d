# Proyecto: Clasificación de Escenas Acústicas con Deep Learning  
**Asignatura:** ACUS 220 Acústica Computacional con Python  
**Modalidad:** Trabajo individual  
**Estudiante:** José Manuel Godoy

---

## 1. Contexto general

El cuadernillo desarrolla un **modelo de clasificación de escenas acústicas** usando el dataset **TUT Acoustic Scenes 2016 (DCASE 2016 Task 1)**.  
Se implementan dos enfoques:

1) **Modelo 1 (3 clases):** *Exterior / Interior / Vehículo* (agrupación de 15 escenas).  
2) **Modelo 2 (15 clases):** clasificación completa de escenas.

El proyecto está **bien estructurado y ejecutable**, con extracción de **log-mel spectrograms** y entrenamiento de una **CNN en PyTorch**, además de una **interfaz (Tkinter) de prueba** con audios reales (grabaciones manuales y ejemplos externos). Se valora especialmente el intento de **validación fuera de dominio** (real recordings), que es un paso más allá de lo exigido en el curso.

Cabe destacar además que el estudiante **participó activamente durante el desarrollo del curso**, realizando preguntas pertinentes en clases y mostrando interés constante por comprender los fundamentos detrás de los modelos implementados. Asimismo, **asistió voluntariamente a la actividad de exposición de proyectos**, donde presentó su trabajo de forma clara y ordenada, demostrando **buena capacidad de comunicación técnica** y dominio general del pipeline desarrollado.

Como puntos a fortalecer: el segundo modelo (15 clases) muestra **baja generalización** y el análisis podría profundizar en: métricas por clase (macro-F1), balance de clases, regularización/early stopping, y estrategias de adaptación de dominio (data augmentation o fine-tuning).

---

## 2. Evaluación por criterios (Hitos 2 y 3)

| Criterio | Peso | Nota | Comentario |
|--------|------:|----:|------------|
| Claridad del planteamiento del problema | 0.15 | 6.7 | Objetivo claro: entrenar 2 modelos (3 y 15 clases) y luego probarlos en audios reales; buena delimitación del alcance. |
| Justificación y contexto del experimento | 0.10 | 6.3 | Contextualización correcta del dataset TUT2016/DCASE; faltan 1–2 referencias más actuales o discusión breve sobre *domain shift* al pasar a grabaciones reales. |
| Metodología y organización del notebook | 0.20 | 6.7 | Flujo ordenado: EDA → extracción log-mel → splits → entrenamiento → evaluación → prueba con interfaz; reproducible. Se sugiere fijar *seeds* y documentar mejor preprocesamiento (duración, normalización, padding/recorte). |
| Calidad del código y buenas prácticas | 0.15 | 6.4 | Código en general claro; hay duplicación de bloques (definición de modelo/procesamiento), doble guardado `np.save`, y poca modularización. Recomendable separar en funciones/módulos y controlar configuración con un diccionario o argumentos. |
| Análisis de resultados y visualizaciones | 0.15 | 6.3 | Buen uso de curvas de pérdida y matrices de confusión; reporte de accuracy correcto. Para 15 clases, sería importante agregar **macro-F1/precision/recall por clase** y analizar confusiones dominantes. |
| Conclusiones y coherencia con objetivos | 0.15 | 6.6 | Conclusiones alineadas: compara 3 vs 15 clases y reconoce el problema de desajuste con audios reales; propone soluciones razonables (augmentation, normalización, fine-tuning). |
| Redacción, ortografía y estilo general | 0.10 | 6.3 | Redacción comprensible y técnica; hay detalles de ortografía/acentos (“preparacion”, “exploratiorio”, “caracterísitcas”) y consistencia de términos que pueden mejorarse. |

**Nota Hitos 2 y 3 (ponderada): 6.5**

---

## 3. Nota final del curso

- **Nota Hito 1:** 6.5  
- **Nota Hitos 2 y 3:** 6.5  

**Nota final del curso:** **6.5**

---

## 4. Comentario global de cierre

El trabajo demuestra una implementación sólida de un pipeline de **clasificación de escenas acústicas** con CNNs en PyTorch: extracción de log-mel, entrenamiento en GPU, evaluación cuantitativa y visualización de resultados. Se valora especialmente el paso adicional de **probar el sistema con grabaciones reales** y la construcción de una **interfaz interactiva** para inspeccionar probabilidades y espectrogramas.

Desde el punto de vista formativo, es importante destacar la **participación activa del estudiante en clases**, así como su **presentación voluntaria del proyecto**, realizada con claridad y buen manejo conceptual. Este aspecto refleja un compromiso académico que complementa adecuadamente el desarrollo técnico del trabajo.

Para seguir mejorando, el foco debiese estar en la **interpretación crítica** del segundo modelo (15 clases) y en estrategias para enfrentar el **cambio de dominio**: reportar métricas robustas (macro-F1), analizar clases con mayor confusión, aplicar **early stopping**, y explorar **data augmentation** o **fine-tuning** con un conjunto pequeño de audios reales etiquetados.

En síntesis, se trata de un proyecto **bien logrado, serio y con proyección**, que evidencia aprendizaje efectivo y una actitud académica muy positiva durante el curso.

**Buen trabajo y felicitaciones por el compromiso mostrado a lo largo del semestre.**