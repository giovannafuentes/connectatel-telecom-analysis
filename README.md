# 📱 Análisis de uso de servicios móviles – ConnectaTel

Proyecto del bootcamp **Data Analyst de TripleTen** (Sprint 7).

## 🎯 Objetivo
Analizar cómo los clientes de ConnectaTel (México y Colombia) usan realmente sus servicios de llamadas y mensajes, para identificar patrones de uso, detectar comportamientos atípicos y segmentar a los clientes, con el fin de optimizar la oferta de planes.

## 📂 Datasets
| Archivo | Contenido |
|---|---|
| `plans.csv` | Catálogo de planes (Básico y Premium): precio, minutos, mensajes y GB incluidos |
| `users_latam.csv` | 4,000 clientes: edad, ciudad, fecha de registro, plan y fecha de cancelación |
| `usage.csv` | 40,000 registros de uso durante 2024: llamadas (duración) y mensajes (longitud) |

## 🔄 Etapas del análisis
1. **Carga y exploración** de la estructura de los 3 datasets.
2. **Diagnóstico de calidad**: valores nulos, sentinels (`-999`, `"?"`) y fechas fuera de rango.
3. **Limpieza**: imputación con mediana, conversión a nulos y verificación de nulos MAR.
4. **Estadística descriptiva** de uso por usuario (tabla agregada y merge).
5. **Visualización y outliers**: histogramas por plan, boxplots y método IQR.
6. **Segmentación** de clientes por nivel de uso y por edad.
7. **Insight ejecutivo** con recomendaciones comerciales.

## 💡 Hallazgos principales
- Los planes están **sobredimensionados**: la mediana de uso en todo 2024 (5 mensajes, 4 llamadas y ~20 minutos) queda muy por debajo de lo incluido cada mes.
- Los usuarios **Premium no consumen más que los Básico**, lo que pone en duda su valor percibido.
- **~73%** de los clientes tiene uso medio, **~20%** bajo y solo **~7%** alto.
- La edad **no determina** el nivel de uso ni el plan contratado.
- Existe un grupo de **alto consumo de minutos (120–155)** que conviene revisar.

## 🛠️ Herramientas
Python · pandas · numpy · matplotlib · seaborn · Jupyter Notebook

## ▶️ Cómo ejecutar el notebook
1. Clona o descarga este repositorio.
2. Abre el notebook en **Jupyter Notebook** o en **Google Colab** (File → Upload notebook).
3. Descarga los 3 archivos CSV y ajusta las rutas en la celda de carga (`pd.read_csv(...)`) si es necesario.
4. Ejecuta todas las celdas en orden: **Run → Run All Cells**.

## 👩‍💻 Autora
**Giovanna Fuentes** – Senior Executive Assistant | Business Operations & Data Analysis
[LinkedIn](https://linkedin.com/in/giovanna-fuentes)
