case-02-discriminant-analysis

# Contexto del negocio
Actualmente manejan un criterio de predicción del 28% en promedio para perfiles default.
Como consultores, nuestro objetivo es construir un modelo de clasificación que pueda predecir el estado de su estatus de deuda (Loan Status),
para que el equipo de LendSmart pueda tomar decisiones informadas basado en la probabilidad de que un cliente sea de alto riesgo o uno seguro para darle un crédito. 
Para ello se aplicarán dos modelos de clasificación de análisis discriminante, uno lineal y otro cuadrático, con el objetivo de observar cual es el que brinda mejores resultados para la empresa.

# Metodología
Se usara análisis discriminante lineal y cuádratico para categorizar a los clientes según su estado de prestamos. Esto ayudara a determinar si son clientes a los que LendSmart debe de 
prestar o si son perfiles que pueden generar deudas. La razón de esto, es porque se busca un método supervisado que sea capaz de clasificar a los clientes.

Librerías:
- pandas as pd
- matplotlib.pyplot as plt
- seaborn as sns
- sklearn
- sklearn.preprocessing import OneHotEncoder
- sklearn.model_selection import train_test_split
- sklearn.preprocessing import MinMaxScaler

  # Datos
  Hay 2499 clientes sin valores nulos y tienen variables descriptivas del cliente. Estas son las variables de dataset: application_id, application_date, loan_amount, annual_income
employment_years, job_stability_score, credit_score, credit_utilization, payment_history_score, open_credit_lines, debt_to_income_ratio, savings_ratio, asset_value, age, education_level,
 marital_status, residential_stability,loan_status

# Hallazgos principales
* Se encontraron las 5 variables que más influyen a tener un cliente con deudas default.
*  Hay elementos que influyen a que la persona tenga una probabilidad menor de tener deudas y viceversa.
* Cuando una persona tiene un buen historial crediticio, estabilidad laboral y un un buen score crediticio, esta suele ser clasificada como alguien que tiene un estatus de préstamo favorable.
* Si una persona gasta más de lo que tiene en su crédito y si tiene un nivel alto de deuda, entonces, esta se suele clasificar como alguien de alto riesgo.

<img width="623" height="556" alt="image" src="https://github.com/user-attachments/assets/2cf48ffb-4353-4445-8426-8a918db1528c" />

Para medir el desempeño del modelo se uso una curva ROC, métricas de accuracy, recall, precision y F1 - Score. En ambos modelos se obtuvo un 100% para todas las métricas.

# Recomendaciones de negocio
* Se recomienda que la empresa utilice el modelo QDA si lo que se busca es rapidez
*  Si el objetivo es la interpretación, se recomienda LDA, ya que, ambos casos presentan los mismos resultados.
*  Al utilizar este modelo, se estima que la empresa logre evitar el 100% de las personas con estatus default, por lo que, LendSmart lograra reducir su cartera de préstamos actual de la empresa .
* Se recomienda que en un futuro se explore más acerca de las características que estos perfiles de alto riesgo tienen.
* Este tipo de investigación y clasificación debe de evitar tener sesgos discriminatorios que excluyan a un cierto grupo de personas.

