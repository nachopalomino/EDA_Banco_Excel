# Análisis de la Tasa de Abandono - Banco Santander

## 📌 1. Contexto y Problemática Actual

El Banco Santander, una entidad financiera con una fuerte presencia en España, Francia y Alemania, ha experimentado un aumento en la tasa de abandono de clientes en los últimos años. A pesar de su variada oferta de productos financieros y servicios digitales, la lealtad de los clientes sigue siendo un desafío, afectando sus ingresos y estabilidad en el mercado.

Ante esta situación, la dirección del banco ha decidido analizar los datos de su base de clientes para identificar patrones de comportamiento y diseñar estrategias efectivas que mejoren la experiencia bancaria y reduzcan la tasa de abandono (churn).

### 🔍 Problemática Detectada

El equipo de análisis de datos ha identificado varios factores de riesgo:

Alta tasa de abandono: Se ha detectado que muchos clientes han dejado de usar los servicios del banco. Es clave analizar las características comunes de estos clientes (edad, saldo, número de productos, actividad, etc.).

Baja participación en productos financieros: Muchos clientes solo utilizan un producto bancario, lo que puede indicar una baja fidelización o desconocimiento de otras opciones disponibles.

Factores demográficos y geográficos: Es necesario examinar si existen diferencias en el comportamiento de abandono según país de residencia, edad, género o ingresos.

Relación entre crédito y abandono: Se evaluará si el Credit Score de un cliente influye en su propensión a abandonar el banco.

Clientes inactivos: Un número considerable de clientes no utiliza activamente su cuenta, lo que podría ser una señal de riesgo de abandono.

## 🎯 2. Objetivo Principal del Proyecto

Este proyecto tiene como objetivo desarrollar un Dashboard interactivo en Excel que permita visualizar y analizar la información clave de la base de clientes del Banco Santander.

A través de este Dashboard, la dirección podrá:

- Identificar **perfiles de clientes propensos al abandono**.

- Detectar **oportunidades para mejorar la retención**, como clientes con pocos productos o inactivos.

- **Analizar tendencias** según país, edad y nivel de ingresos.

- Evaluar la relación entre el **Credit Score** y la **retención de clientes**.

##  3. Estructura del Repositorio
```bash
|------ data
  |---- Churn_Modelling.csv  #Datos originales
|------ Excels
```


## 📊 4. Descripción del Conjunto de Datos

Este análisis se basa en un conjunto de datos proporcionado por el Banco Santander, que contiene información detallada sobre sus clientes en España, Francia y Alemania.

Cada fila representa un cliente único y cada columna almacena información relevante sobre su perfil, comportamiento financiero y relación con el banco. A continuación, se describen las principales variables:

### 🏷 **Identificación del Cliente**

- **Customer_ID**: Identificador único del cliente.

- **Surname**: Apellido del cliente.

### 🌍 **Identificación Demográfica**

- **Geography**: País de residencia (España, Francia, Alemania).

- **Gender**: Género (Masculino/Femenino).

- **Age**: Edad del cliente en años.

### 🏦 **Relación con el Banco**

- **Tenure**: Años que el cliente ha sido parte del banco.

- **NumOfProducts**: Cantidad de productos financieros contratados.

- **HasCrCard**: Posee tarjeta de crédito (1 = Sí, 0 = No).

- **IsActiveMember**: Cliente activo (1 = Sí, 0 = No).

### 💰 **Información Financiera**

- **Credit_Score**: Puntuación crediticia del cliente.

- **Balance**: Saldo actual en la cuenta.

- **Estimated_Salary**: Estimación del salario anual.

### 🚪 **Estado del Cliente**

- **Exited**: Variable objetivo (1 = Cliente abandonó, 0 = Cliente retenido).

### 📈 **Variables Derivadas para Análisis**

- **Segmento_de_Edad**: Agrupación en rangos etarios (ej. 18-30, 31-40, etc.).

- **Categoría_de_Saldo**: Clasificación en Bajo (<10,000), Medio (10,000-100,000) y Alto (>100,000).

- **Engagement_Score**: Indicador basado en la actividad del cliente y número de productos contratados.

Este dataset permitirá realizar un análisis detallado del comportamiento de los clientes y detectar patrones de fidelización o abandono.

## 〽️ 5. Análisis Descriptivo de Variables Numéricas

A continuación, se detallan las conclusiones sobre el análisis descriptivo de las variables numéricas de nuetro conjunto de datos proporcionado por el banco:

- **Credit Score**: La distribución del Credit Score es **simétrica y mesocúrtica**, lo que sugiere que los datos están bien distribuidos alrededor de la media sin sesgos significativos. La baja desviación estándar y el bajo error típico indican que la media es un buen representante del valor central de la distribución. El boxplot refuerza la conclusión de que El Credit Score está distribuido de manera simétrica alrededor de la mediana, con una dispersión moderada y valores atípicos que podrían ser importantes para análisis más detallados, como la identificación de segmentos específicos de la población con características crediticias particulares.
- **Edad**: La distribución de las edades muestra una **ligera asimetría positiva**. La mayoría de los individuos se concentran en edades más jóvenes, aunque hay una cola extendida hacia edades más avanzadas. La distribución es **leptocúrtica**, indicando un pico más pronunciado y una mayor concentración de datos alrededor de la media. La dispersión de las edades es moderada, con un rango de 74 años. En general, los datos sugieren una población predominantemente joven, con una presencia significativa de individuos en edades más altas.
- **Tenure**: La distribución de la permanencia (tenure) muestra una **ligera asimetría positiva**, con una media de 39 y una mediana de 37. La mayoría de los individuos tienen períodos de permanencia más cortos, pero hay una cola extendida hacia valores más altos, indicando que un grupo significativo tiene una permanencia mucho más larga. La distribución es **leptocúrtica**, con una concentración de datos alrededor de la media y una dispersión moderada. En general, los datos sugieren que, aunque la mayoría de los clientes tienen una permanencia relativamente corta, existe un segmento con una permanencia considerablemente más larga.
- **Balance**: La distribución del balance muestra una **ligera asimetría positiva**. La mayoría de los individuos tienen saldos más bajos, pero hay una cola extendida hacia valores más altos, indicando que un grupo significativo tiene saldos considerablemente más elevados. La distribución es **leptocúrtica**, con una concentración de datos alrededor de la media y una dispersión moderada. En general, los datos sugieren que, aunque la mayoría de los clientes tienen saldos relativamente bajos, existe un segmento con saldos mucho más altos.
- **Productos**: La distribución del número de productos muestra una **ligera asimetría positiva**. La mayoría de los clientes tienen un número moderado de productos, pero hay una cola extendida hacia valores más altos, indicando que un grupo significativo posee una cantidad considerablemente mayor de productos. La distribución es **leptocúrtica**, lo que sugiere una mayor concentración de datos alrededor de la media y una dispersión moderada. En general, los datos reflejan que, aunque la mayoría de los clientes tienen un número relativamente bajo de productos, existe un segmento con una cantidad mucho más alta.
- **Salario**: La distribución de los salarios muestra una **ligera asimetría positiva**. La mayoría de los empleados tienen salarios más bajos, pero existe una cola extendida hacia valores más altos, indicando que un grupo significativo tiene salarios considerablemente más elevados. La distribución es **leptocúrtica**, lo que sugiere una mayor concentración de datos alrededor de la media y una dispersión moderada. En general, los datos reflejan que, aunque la mayoría de los empleados tienen salarios relativamente bajos, hay un segmento con salarios mucho más altos.


## 🚀 6. Próximos Pasos

Para optimizar la retención y fidelización de clientes, se seguirán estos pasos clave:

#### 1️⃣ Recepción de los datos completos 📥

Verificación de integridad y estructura de la información.

#### 2️⃣ Análisis Exploratorio de Datos (EDA) 🔍

Identificación de patrones, relaciones entre variables y detección de datos atípicos.

#### 3️⃣ Diseño de Dashboards en Excel 📊

Creación de visualizaciones interactivas con KPIs clave.

#### 4️⃣ Presentación de Resultados 📢

Exposición de hallazgos junto con estrategias basadas en datos para mejorar la retención de clientes.

✅ Este proyecto proporcionará al Banco Santander herramientas prácticas y basadas en datos para reducir la tasa de abandono y mejorar la experiencia del cliente.

