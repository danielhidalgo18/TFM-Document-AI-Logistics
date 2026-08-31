# Estudio comparativo de modelos de aprendizaje profundo para el tratamiento de documentación logística industrial

Este repositorio contiene el código fuente y los materiales complementarios asociados al Trabajo de Fin de Máster.

## Resumen

El sector de la logística industrial genera diariamente un gran volumen de albaranes y documentos mercantiles cuya digitalización y procesamiento manual suponen un importante cuello de botella operativo y económico. La automatización de este flujo presenta desafíos relevantes como la confidencialidad de los datos, la elevada diversidad de formatos y el deterioro físico de los documentos en los entornos de trabajo constituyen factores que limitan significativamente la eficacia de los sistemas tradicionales basados en reglas.

Para abordar estos retos, el presente trabajo propone un estudio empírico y comparativo de técnicas avanzadas de Inteligencia Artificial Documental orientadas a la extracción de información clave. Los algoritmos seleccionados representan el estado del arte actual y pueden desplegarse en entornos locales, garantizando la soberanía del dato.

Desde el punto de vista metodológico, se utiliza inicialmente un conjunto de datos público para evaluar los modelos preentrenados y establecer una línea base de referencia. Posteriormente, se lleva a cabo un proceso de ajuste fino sobre un conjunto de datos sintético desarrollado específicamente para este trabajo, con el objetivo de adaptar los modelos al dominio logístico. Una vez completada esta adaptación, se introduce ruido visual controlado para analizar su impacto sobre el rendimiento de los distintos enfoques.

Los resultados muestran que, bajo condiciones visuales favorables, arquitecturas multimodales como LayoutLMv3 alcanzan una elevada capacidad de extracción. Sin embargo, su rendimiento se reduce de forma notable ante altos niveles de degradación visual, debido a la propagación de errores procedentes del sistema de reconocimiento óptico de caracteres del que dependen. Por el contrario, el modelo generativo DONUT presenta una mayor robustez en escenarios visualmente adversos y adopta una estrategia de predicción más conservadora, orientada a minimizar las extracciones incorrectas.

En términos de eficiencia operativa, DONUT reduce significativamente los costes, tiempos de entrenamiento y mantiene una latencia de inferencia más estable frente a documentos degradados. En conjunto, los resultados indican que este paradigma generativo constituye la alternativa más adecuada para su despliegue en entornos productivos, al ofrecer el mejor equilibrio entre rendimiento, eficiencia y fiabilidad operativa.

**Palabras clave:** Inteligencia Artificial Documental, Extracción de Información Clave, Logística Industrial.

---

## Arquitecturas Evaluadas

Este proyecto evalúa y compara tres paradigmas diferentes de IA Documental:

*   **PaddleOCR + Expresiones Regulares:** Pipeline tradicional basado en reglas.
*   **LayoutLMv3:** Transformer Multimodal (consciente del *layout*).
*   **DONUT:** Transformer de Comprensión Documental (generativo de extremo a extremo y *OCR-free*).

---

## Estructura del Repositorio

```text
.
├── src/
│   ├── data_generation/
│   ├── augmentation/
│   ├── training/
│   ├── evaluation/
│   └── visualization/
│
├── examples/
│   ├── images/
│   └── annotations/
│
├── results/
│   ├── figures/
│   └── tables/
│
├── docs/
│   └── TFM__Daniel_Hidalgo_Ocana_2026-07-22.pdf
│
├── requirements.txt
├── LICENSE
└── README.md
