case-01-factor-analysis

## Contexto de negocio
Entender la opinión de los clientes dentro de la empresa TechnoServe, es de alta importancia porque, a partir de esto, se pueden encontrar estrategias diseñadas para mejorar
la atención del cliente y el servicio. Lo cual, puede repercutir en la cantidad de retención de clientes que se tiene y el crecimiento del negocio. 
Por esto, el objetivo, de este proyecto, será encontrar los factores que influyen más en los clientes y proponer un plan de acción enfocado en mejorar los servicios que influyen
más en la opinión del cliente.


## Metodología
Se utiliza factor de análisis para encontrar factores latentes en las opiniones de los clientes. 
Esto es porque a partir del análisis de correlación, se identificaron agrupamientos entre las variables de satisfacción que comparten patrones similares y se relacionan entre sí. 
Además de haber correlaciones entre variables de la misma área, también existen correlaciones entre diferentes áreas, como Technical Excellence & Innovation y Project Delivery.
Por ende, aunque se puede generar un agrupamiento por áreas, se ha identificado, que también existe una correlación entre áreas, lo que sugiere que existen factores latentes que pueden estar
influyendo en estos resultados.


Librerías: 
- numpy as np
- matplotlib.pyplot as plt
- pandas as pd
- seaborn as sns
- factor_analyzer import FactorAnalyzer
- factor_analyzer.factor_analyzer import calculate_kmo
- sklearn.decomposition import PCA
- sklearn.linear_model import LinearRegression


## Descripción de dataset
**File**: `customer_satisfaction_data.csv`  
**Observaciones**: 3,400 respuestas   
**Clientes**: 850  clientes  
**Periodo de tiempo**: Q1-Q4 2024 
**Tasa de respuesta**: 78% 
Variables:
`technical_expertise`, `problem_solving`, `innovation_solutions`,
`technical_documentation`, `system_integration`,
`account_manager_responsive`, `executive_access`, `trust_reliability`,
`long_term_partnership` `communication_clarity`,
`project_management`, `timeline_adherence`, `budget_control`, `quality_deliverables` `change_management`,
`cost_transparency`, `value_for_money` `roi_demonstration`,
`competitive_pricing`, `billing_accuracy`, `support_responsiveness`, `training_quality` y `documentation_help`.


Por su parte, también hay 5 variables que muestran los resultados obtenidos en la encuesta, donde se tiene:
- **`overall_satisfaction`** (1-7): Satisfacción general de las soluciones de TechnoServe
- **`nps_score`** (0-10): probabilidad de recomendación.
- **`renewal_likelihood`** (1-5): probabilidad de que el cliente renueve el contrato.
- **`revenue_growth_pct`** (continúa): crecimiento año con año de la empresa.
- **`referrals_generated`** (entero): número de referencias por trimestre.


## Hallazgos principales
Se encontrar tres factores latentes:
Excelencia Técnica e Innovación: esperan tener un servicio técnico donde se les otorgue proyectos de calidad.
Relación y comunicación estratégica: los clientes buscan tener una relación de confianza y de comunicación con la consultoría. 
Gestión de Proyectos y Calidad Operativa: los clientes esperan tener un servicio donde los resultados sean entregados en tiempo y forma.

<img width="808" height="675" alt="image" src="https://github.com/user-attachments/assets/dcac1516-8e75-403a-bf70-9a7897e2340f" />

Para determinar los factores latentes, se utilizaron los valores de las cargas de factores y se realizaron matrices de correlación, para verificar si los resultados era coherentes.

# Recomendaciones de negocio
Implementar prácticas mensuales con casos simulados, enfocados en la resolución de problemas reales y la generación de soluciones innovadoras. 
Impacto esperado:
+5.5% en la satisfacción general de los clientes.
+6% en la probabilidad de renovación.
+ 3.25% en crecimiento de ingresos interanuales (cuentas específicas).


Fortalecer, la calidad de relación con el cliente, permitirá establecer relaciones de respeto y lealtad con los clientes.
Se sugiere asignar a los perfiles con mayores habilidades comunicativas como los actores principales para contactar a los clientes. 
Realizar evaluaciones psicométricas anuales para identificar las fortalezas de cada trabajador. 
Fomentar la comunicación efectiva mediante actividades de integración mensuales orientadas al trabajo en equipo y colaboración.

Impacto esperado:
+5% satisfacción general del cliente.
+5.62% de probabilidad de renovación
 +4.66% de la probabilidad de recomendación.

Establecer planes de proyectos con revisiones semanales, donde se presenten los avances realizados y las mejoras que se pueden implementar
Impacto esperado:
+5% satisfacción general.
+5.58% probabilidad de renovación.
+4.66% probabilidad de recomendación.



