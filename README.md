# 📊 Análisis de Tarifas de Megaline

Este proyecto fue desarrollado como parte de un análisis de negocio para el operador de telecomunicaciones **Megaline**, con el objetivo de determinar cuál de sus dos planes de prepago —**Surf** o **Ultimate**— genera más ingresos.  

El análisis se basa en los datos de **500 clientes** y busca identificar patrones de comportamiento, consumo de servicios y diferencias estadísticas en los ingresos entre ambas tarifas.

## 🎯 Objetivo del proyecto

El departamento comercial de Megaline desea optimizar el presupuesto publicitario identificando cuál de las dos tarifas de prepago (**Surf** o **Ultimate**) resulta más rentable.  

El propósito del análisis es:
- Explorar el comportamiento de los clientes (llamadas, mensajes y tráfico web).
- Calcular los ingresos generados por cada usuario.
- Comparar los ingresos promedio de ambas tarifas mediante **pruebas estadísticas**.
- Proporcionar recomendaciones basadas en los hallazgos.

## 🧠 Contexto de negocio

Megaline ofrece dos planes de prepago con las siguientes características:

| Plan | Cuota mensual | Minutos incluidos | SMS incluidos | Datos incluidos | Exceso por min | Exceso por SMS | Exceso por GB |
|------|----------------|-------------------|----------------|-----------------|----------------|----------------|----------------|
| **Surf** | $20 | 500 | 50 | 15 GB | $0.03 | $0.03 | $10 |
| **Ultimate** | $70 | 3000 | 1000 | 30 GB | $0.01 | $0.01 | $7 |

> 🔹 Megaline redondea los segundos a minutos y los megabytes a gigabytes.  
> Las llamadas se redondean por cada evento (aunque dure 1 segundo), y el tráfico web se redondea al alza sobre el total mensual.

## 🧩 Estructura de los datos

El análisis se basa en **cinco tablas**:

| Tabla | Descripción |
|--------|--------------|
| `users` | Datos demográficos y plan contratado por cada usuario. |
| `calls` | Registros de llamadas con fecha y duración. |
| `messages` | Registros de mensajes enviados. |
| `internet` | Registros de sesiones de datos (MB utilizados). |
| `plans` | Detalle de los planes y sus costos. |

## 🧰 Herramientas utilizadas

- **Python** 🐍  
- **Pandas**, **NumPy** — Limpieza y análisis de datos  
- **Matplotlib**, **Seaborn** — Visualización  
- **SciPy** — Pruebas estadísticas  
- **Jupyter Notebook** — Entorno de desarrollo interactivo  

## 📈 Metodología

1. **Carga y exploración de datos**  
   Revisión de las tablas, detección de valores nulos y comprensión de las relaciones.

2. **Limpieza y transformación**  
   - Conversión de tipos de datos (fechas, numéricos).  
   - Agrupación mensual por usuario.  
   - Cálculo de minutos, mensajes y tráfico total.

3. **Cálculo de ingresos**  
   - Cálculo de ingresos mensuales considerando la cuota fija y el exceso de uso.

4. **Análisis exploratorio (EDA)**  
   - Distribución de consumo entre usuarios.  
   - Comparación de ingresos por plan.  
   - Identificación de patrones por edad o ciudad.

5. **Prueba estadística**  
   - Hipótesis: “No hay diferencia significativa en los ingresos medios entre los planes Surf y Ultimate”.  
   - Aplicación de **prueba t de Student** para evaluar la hipótesis.

6. **Conclusiones y recomendaciones**  
   - Determinar el plan más rentable.  
   - Proponer estrategias para maximizar la rentabilidad.

## 📊 Resultados esperados

- Identificación de diferencias significativas entre los ingresos medios de los planes.  
- Determinación del plan que genera **mayor rentabilidad promedio**.  
- Insights sobre el comportamiento de los clientes por ciudad, edad y tipo de consumo.
