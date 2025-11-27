# mi-portfolio-ma2003b
Integrantes: Paulina Leal Mosqueda y Santiago Nava Figueroa

Este portafolio reúne los principles casos prácticos desarrollados a lo largo del curso MA2003B, con el prooósito de demostrar dominio en herramientas estadísticas, análisis exploratorio de datos, modelación y elaboración de reportes técnicos. Cada caso está diseñado para utilizar diferentes herremientas, como PCA, análisis por factores, LDA, QDA y clustering. 

El objetivo del portafolio es documentar los procesos de análisis completos, incluyendo código, resultados, interpretación y reportes ejecutivos, siguiendo un enfoque reproducible y profesional. Los códigos generados en estas carpetas son mediante el lenguaje de Python. 

En particular, se generaron tres diferentes proyectos, cada uno enfocado en situaciones hipóteticas distintas. La primer carpeta ´´factor analysis,'' se enfoca primordialmente en un caso proctco para entender la satisfacción de los clientes y generar estrategias para mejorar el servicio en una consultoría. Por su parte, el segundo proyecto, de ''discriminant analysis,'' esta enfocado en clasificar clientes con scores default o no en términos de deudas y prestamos. Por último, se presenta un proyecto de agrupación de clientes, para poder identificar los diferentes grupos que una empresa de e-commerce tiene y a partir de ello generar estrategias de valor.


##  Resumen de casos

| **Caso** | **Método** | **Pregunta de Negocio** | **Hallazgo Clave** | **Link** |
|---------|------------|--------------------------|--------------------|----------|
| TechnoServe Customer Satisfaction | Factor Analysis | ¿Qué dimensiones latentes impulsan la satisfacción del cliente? | La satisfacción general está explicada en un 60% siendo *Excelencia Técnica* el factor más importante | [Ver caso →](./case-01-factor-analysis/) |
| LendSmart Credit Risk | Discriminant Analysis | ¿Cómo clasificar aplicantes de crédito en categorías de riesgo? | Modelo con 100% en todas las métricas para QDA y LDA| [Ver caso →](./case-02-discriminant-analysis/)  |
| ShopSmart Customer Segmentation | Cluster Analysis | ¿Qué segmentos naturales existen en la base de clientes? | 5 clusters identificados; *High-Value Loyalists* representan 18% pero generan 45% de los ingresos | *Link pendiente* |


##  Instrucciones de reproducibilidad


## Estructura del repositorio
```md
mi-portfolio-ma2003b/
│
├── README.md                  # Descripción general del portafolio
├── LICENSE                    # Licencia del proyecto
├── requirements.txt           # Dependencias para reproducibilidad
├── .gitignore                 # Archivos ignorados por Git
│
├── case-01-factor-analysis/
│   ├── README.md              # Documentación del caso 01
│   ├── data/                  # Datos utilizados
│   ├── notebooks/             # Notebook(s) con el análisis
│   ├── reports/               # Reporte ejecutivo y técnico
│   ├── src/                   # Funciones auxiliares
│   └── visualizations/        # Gráficas generadas
│
├── case-02-credit-risk/
│   ├── README.md
│   ├── data/
│   ├── notebooks/
│   ├── reports/
│   ├── src/
│   └── visualizations/
│
└── case-03-customer-segmentation/
    ├── README.md
    ├── data/
    ├── notebooks/
    ├── reports/
    ├── src/
    └── visualizations/
```
