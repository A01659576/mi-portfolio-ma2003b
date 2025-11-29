### Comparación de métodos multivariados

| Aspecto | Factor Analysis | Discriminant Analysis | Cluster Analysis |
|---|---:|---:|---:|
| Tipo de aprendizaje | No supervisado | Supervisado | No supervisado |
| Objetivo principal | Reducción de dimensionalidad | Clasificación | Segmentación |
| Input requerido | Variables continuas u ordinales | Variable categórica (clase) + predictores continuos o categóricos | Variables continuas u ordinales; puede manejar mixtas con distancias adecuadas |
| Output principal | Factores latentes y cargas factoriales | Funciones discriminantes y reglas de clasificación | Grupos/clusters, centroides y medidas de similitud |
| Caso de uso ideal | Construcción de índices, síntesis de variables y preprocesamiento para otros modelos | Scoring, predicción de pertenencia a clases y validación de grupos conocidos | Segmentación de clientes, detección de patrones y exploración de subpoblaciones |
| Limitaciones | Supone relaciones lineales y correlación entre variables; interpretación subjetiva; sensible al escalado y a valores atípicos | Requiere etiquetas de clase; LDA asume homocedasticidad y normalidad; sensible a outliers y multicolinealidad | Elección del número de clusters es arbitraria; sensible a escala, inicialización y ruido; validación e interpretación pueden ser subjetivas |