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

## 🚀 5. Próximos Pasos

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

