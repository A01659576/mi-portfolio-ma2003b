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

1. **Escalado (*Scaling*):** Todas las variables fueron escaladas utilizando el método **StandardScaler** o **MinMaxScaler** (dependiendo del código, especificar aquí) para asegurar que ninguna métrica dominara la distancia euclidiana en el algoritmo K-Means.
2. **Determinación del Número Óptimo de Clusters (K):** Se utilizó el método del **Codo (*Elbow Method*)** y/o el **Coeficiente de Silueta (*Silhouette Score*)** para determinar el valor óptimo de $K=4$.

### 3.  Resultados y Hallazgos Clave

Se identificaron **5 *clusters*** principales. La tabla a continuación resume el perfil promedio de cada grupo (valores desescalados):


| Métrica                     | Cluster 0   | Cluster 1 | Cluster 2 | Cluster 3 |
| :--------------------------- | :---------- | :-------- | :-------- | :-------- |
| **recency\_days**            | 8.02        | 35.59     | 19.84     | 14.53     |
| **monthly\_transactions**    | 14.07       | 1.68      | 4.04      | 6.59      |
| **total\_spend**             | **6507.29** | 422.62    | 3875.94   | 1450.95   |
| **avg\_basket\_size**        | 22.03       | 3.05      | 18.17     | 5.56      |
| **return\_rate**             | 0.1         | 0.27      | **0.24**  | 0.13      |
| **email\_open\_rate**        | 0.58        | 0.37      | 0.45      | **0.44**  |
| **customer\_tenure\_months** | 45.92**     | 52.31     | 22.36     | 29.6      |

### 4.  Perfiles Accionables de los Clusters


| ID    | Nombre Propuesto del Cluster                 | Características Distintivas                                                                      | Estrategia de Negocio Sugerida                                                                                |
| :---- | :------------------------------------------- | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------ |
| **0** | **Clientes Premium / De Alto Valor (VIP)**   | Frecuentes y con compras altas                                                                    | Estrategias de retención exclusivas, programas de lealtad, comunicación de productos*premium*.              |
| **1** | **Window Shoppers** |   Son un 30% de la población. Observan los productos por varios minutos, pero no compran en grandes cantidades ni suelen frecuentar el sitio.| Realizar ofertas para productos de bajo precio, mantener ofertas de productos para atraer más su atención.  |
| **2** | **Clientes express**                         |  Son aquellos que no pasan mucho tiempo en la tienda, pero compran productos de alto precio y a cantidades moderadas. Además, tienen un alto nivel de retorno, lo que sugiere que estos clientes realizan compras rápidas, causando que muchas veces se arrepientan de su decisión.   | Desplegar productos que tengan baja probabilidad de retorno, Personalizar su plataforma, para evitar que compren productos que terminen regresando.   |
| **3** | **Clientes potenciales**                     | Son clientes que no compran en grandes cantidades, pero que suelen visitar el sitio y hacer compras moderadas.              | Aumentar Frecuencia de Contacto, incrementar ofertas para lograr entablar una relación entre cliente-tienda, entender su comportamiento y comenzar a ofertar cosas, que podrían gustarle.   |


### 5.  Requerimientos Técnicos

Este proyecto fue desarrollado en:

* Python (versión 3.x)
* Librerías : `pandas`, `numpy`, `scikit-learn` (`KMeans`, `StandardScaler`), `matplotlib`, `seaborn`.
