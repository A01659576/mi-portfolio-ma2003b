## 📄 README.md: Segmentación de Clientes con K-Means

### 1.  Introducción

Este proyecto presenta el análisis de **Segmentación de Clientes** realizado para identificar y caracterizar grupos homogéneos (*clusters*) dentro de la base de datos de la empresa. La segmentación se llevó a cabo utilizando el algoritmo **K-Means** sobre métricas clave de comportamiento transaccional y *web-analytics*.

El objetivo principal es transformar los datos de comportamiento del cliente en segmentos accionables para que los equipos de Marketing, Producto y Servicio al Cliente puedan diseñar estrategias altamente personalizadas y maximizar el Valor de Vida del Cliente (**CLV**).

### 2.  Metodología de *Clustering*

#### 2.1. Ingeniería de Características (*Feature Engineering*)

Las siguientes variables fueron calculadas para cada cliente:


| Métrica                  | Definición                                           |
| :------------------------ | :---------------------------------------------------- |
| `recency_days`            | Días desde la última compra.                        |
| `monthly_transactions`    | Frecuencia de compras promedio mensual.               |
| `total_spend`             | Gasto total acumulado.                                |
| `avg_basket_size`         | Tamaño promedio de la cesta de compra.               |
| `return_rate`             | Tasa de devoluciones sobre el total de compras.       |
| `email_open_rate`         | Tasa de apertura de correos electrónicos.            |
| `product_views_per_visit` | Vistas de productos por sesión de navegación.       |
| `customer_tenure_months`  | Antigüedad del cliente en meses.                     |
| `avg_session_duration`    | Duración promedio de la sesión en segundos/minutos. |

#### 2.2. Preprocesamiento

1. **Escalado (*Scaling*):** Todas las variables fueron escaladas utilizando el método **StandardScaler** para asegurar que ninguna métrica dominara la distancia euclidiana en el algoritmo K-Means.
2. **Determinación del Número Óptimo de Clusters (K):** Se utilizó el método del **Codo (*Elbow Method*)** y/o el **Coeficiente de Silueta (*Silhouette Score*)** para determinar el valor óptimo de $K=4$.

### 3.  Resultados y Hallazgos Clave

Se identificaron **5 *clusters*** principales. La tabla a continuación resume el perfil promedio de cada grupo (valores desescalados):


| Métrica                     | Cluster 0   | Cluster 1 | Cluster 2 | Cluster 3 | Cluster 4  |
| :--------------------------- | :---------- | :-------- | :-------- | :-------- | :--------- |
| **recency\_days**            | 7.94        | 17.86     | 19.87     | 15.29     | 36.73      |
| **monthly\_transactions**    | 14.07       | 4.05      | 4.09      | 7.74      | 1.96       |
| **total\_spend**             | **6541.68** | 1169.29   | 3882.35   | 1472.51   | **440.19** |
| **avg\_basket\_size**        | 22.12       | 4.78      | 18.24     | 5.48      | 3.29       |
| **return\_rate**             | 0.09        | 0.15      | **0.24**  | 0.09      | **0.31**   |
| **email\_open\_rate**        | 0.57        | 0.15      | 0.45      | **0.66**  | 0.43       |
| **customer\_tenure\_months** | **26.08**   | 7.12      | 21.84     | 21.66     | 16.98      |

### 4.  Perfiles Accionables de los Clusters


| ID    | Nombre Propuesto del Cluster                 | Características Distintivas                                                                      | Estrategia de Negocio Sugerida                                                                                |
| :---- | :------------------------------------------- | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------ |
| **0** | **Clientes Premium / De Alto Valor (VIP)**   | Máximo gasto ($6541), máxima frecuencia (14.07 tx/mes) y máxima antigüedad.                   | Estrategias de retención exclusivas, programas de lealtad, comunicación de productos*premium*.              |
| **1** | **Clientes Nuevos / Potenciales**            | Mínima antigüedad (7.12 meses), bajo gasto, baja apertura de correos.                           | Campañas de*onboarding* agresivas, *incentivos* a la segunda y tercera compra, educación sobre el producto. |
| **2** | **Clientes con Fricción / Alto Riesgo**     | Alta antigüedad, pero la tasa de devolución más alta después del Cluster 4 (0.24).            | Identificar causas de devolución (calidad/ajuste). Enfoque en la calidad del producto y servicio postventa.  |
| **3** | **Leales Digitales / Comprometidos**         | Mayor tasa de apertura de correos (0.66), alta navegación. Gasto moderado.                       | *Up-selling* y *cross-selling* dirigidos a través de canales de email, ofertas personalizadas.               |
| **4** | **Clientes Dormidos / Perdidos (*Churned*)** | Máxima*recency* (36.73 días), mínimo gasto y frecuencia. Tasa de devolución más alta (0.31). | Campañas de reactivación (*win-back*) con descuentos significativos o cupones de expiración corta.         |

### 5.  Requerimientos Técnicos

Este proyecto fue desarrollado en:

* Python (versión 3.x)
* Librerías : `pandas`, `numpy`, `scikit-learn` (`KMeans`, `StandardScaler`), `matplotlib`, `seaborn`.
