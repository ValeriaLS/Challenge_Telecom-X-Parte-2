# Challenge_Telecom-X-Parte-2

## Proyecto de Data Science

Este proyecto forma parte de un análisis de datos enfocado en comprender y predecir la cancelación de clientes (Churn) dentro de la empresa ficticia Telecom X.

La cancelación de clientes representa uno de los principales desafíos para las empresas de telecomunicaciones, ya que impacta directamente en los ingresos y en la estabilidad del negocio. Por esta razón, el objetivo de este proyecto es desarrollar modelos predictivos capaces de anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios.

A través de técnicas de análisis exploratorio de datos, preparación de datos y machine learning, se construyó un pipeline que permite identificar patrones relevantes en el comportamiento de los clientes y generar insights estratégicos para mejorar la retención.

# Objetivo del Proyecto

El objetivo principal de este análisis es predecir la cancelación de clientes utilizando modelos de clasificación, a partir de variables relacionadas con:

* Perfil del cliente
* Servicios contratados
* Tipo de contrato
* Métodos de pago
* Cargos mensuales y totales

Con este enfoque, la empresa podría identificar clientes con alto riesgo de abandono y aplicar estrategias de retención antes de que cancelen el servicio.

# Dataset

El dataset utilizado contiene información de clientes de Telecom X, incluyendo características demográficas, servicios contratados y datos de facturación.

Algunas de las variables incluidas son:

* **Gender** – género del cliente
* **Tenure** – tiempo que el cliente lleva con la empresa
* **InternetService** – tipo de servicio de internet
* **Contract** – tipo de contrato
* **PaymentMethod** – método de pago
* **MonthlyCharges** – cargos mensuales
* **TotalCharges** – cargos totales
* **Churn** – variable objetivo que indica si el cliente canceló el servicio


# Pipeline del Proyecto

El flujo de trabajo seguido en este proyecto se compone de varias etapas fundamentales dentro de un proyecto de Data Science:

### 1. Preparación de los Datos

Se realizó un proceso de limpieza y transformación del dataset para garantizar su calidad y compatibilidad con los modelos de machine learning.

Entre las principales tareas se incluyeron:

* Eliminación de variables irrelevantes
* Tratamiento de valores nulos
* Conversión de variables categóricas
* Revisión de consistencia en los datos

### 2. Clasificación de Variables

Las variables fueron clasificadas en dos tipos principales:

**Variables numéricas**

* Tenure
* MonthlyCharges
* TotalCharges

**Variables categóricas**

* Contract
* InternetService
* PaymentMethod
* OnlineSecurity
* TechSupport
* StreamingTV

Esta clasificación permitió aplicar transformaciones adecuadas durante la etapa de preparación de datos.

### 3. Codificación y Normalización

Para preparar los datos para el modelado se aplicaron las siguientes técnicas:

**One-Hot Encoding**

Se utilizó para convertir variables categóricas en variables numéricas binarias.

**Normalización**

Se aplicó escalado a algunas variables numéricas para mejorar el desempeño de ciertos algoritmos de machine learning.


### 4. División de los Datos

El dataset fue dividido en dos subconjuntos:

* **80% para entrenamiento**
* **20% para prueba**

Esto permite evaluar qué tan bien generalizan los modelos con datos que no han sido utilizados durante el entrenamiento.


# Análisis Exploratorio de Datos (EDA)

Antes de entrenar los modelos se realizó un análisis exploratorio de datos para identificar patrones relacionados con la cancelación de clientes.

Algunos de los hallazgos más relevantes incluyen:

### Tipo de contrato y cancelación

Los clientes con contratos mensuales presentan una mayor probabilidad de cancelar el servicio, mientras que aquellos con contratos anuales o de dos años muestran mayor estabilidad.

### Antigüedad del cliente

Se observó que los clientes con menor tiempo en la empresa tienen mayor tendencia a cancelar, lo cual indica que los primeros meses del servicio son críticos para la retención.

### Cargos mensuales

Los clientes con **cargos mensuales más altos** presentan en algunos casos mayor probabilidad de churn, lo cual puede estar relacionado con la percepción de valor del servicio.

# Modelos de Machine Learning

Para la predicción del churn se entrenaron distintos modelos de clasificación, con el objetivo de comparar su rendimiento.

Los modelos utilizados incluyen:

* **Regresión Logística**
* **Random Forest**
* **Regresión Logística Balanceada**

Cada modelo fue evaluado utilizando métricas de clasificación para analizar su capacidad de identificar correctamente a los clientes que cancelan el servicio.

# Evaluación de Modelos

El rendimiento de los modelos se evaluó mediante diferentes métricas:

* **Accuracy**
* **Precision**
* **Recall**
* **F1 Score**
* **Matriz de Confusión**

Estas métricas permiten analizar no solo la precisión general del modelo, sino también su capacidad para detectar correctamente los casos de churn, que son especialmente importantes para la empresa.

# Factores Clave que Influyen en la Cancelación

A partir del análisis y del comportamiento de los modelos, se identificaron algunos factores que influyen significativamente en la cancelación de clientes:

* Contratos mensuales
* Baja antigüedad del cliente
* Cargos mensuales elevados
* Ausencia de servicios adicionales
* Algunos métodos de pago específicos

Estos factores pueden servir como indicadores tempranos de riesgo de cancelación.


# Impacto Estratégico

Los resultados de este análisis pueden ayudar a Telecom X a implementar estrategias para reducir la evasión de clientes, por ejemplo:

* Incentivar contratos de mayor duración
* Mejorar la experiencia del cliente durante los primeros meses
* Ofrecer paquetes de servicios adicionales
* Implementar sistemas de monitoreo predictivo para detectar clientes en riesgo


# Estructura del Proyecto

```
TelecomX-Churn-Prediction
│
├── Challenge_Telecom_X_Parte2.ipynb
│
├── data
│   └── telecomx_datos_tratados.csv

│
└── README.md
```

# Tecnologías Utilizadas

Este proyecto fue desarrollado utilizando herramientas comunes dentro del ecosistema de Data Science:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

# Conclusión

Este proyecto demuestra cómo el análisis de datos y los modelos de machine learning pueden utilizarse para anticipar la cancelación de clientes y apoyar la toma de decisiones estratégicas dentro de una empresa.

A partir de este enfoque predictivo, Telecom X podría implementar acciones preventivas para mejorar la retención de clientes y fortalecer su relación con los usuarios.

