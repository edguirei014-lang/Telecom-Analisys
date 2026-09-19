# Telecom Analysis – Sprint 7

Este repositorio contiene el análisis realizado durante el Sprint 7 del caso Connectatel.

## Objetivo
Evaluar el comportamiento de los clientes de una empresa de telecomunicaciones en Latinoamérica, ConnectaTel, con información registrada hasta el año 2024,

## Datasets utilizados:
1.- plans.csv: Catálogo de planes con sus precios y beneficios.
2- users_latam.csv: Información de cada usuario (datos personales, plan, fecha de registro, churn).
2.- usage.csv: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud.

## Etapas del analisis realizadas
1. Carga y exploración inicial
Se cargaron los tres datasets con `pandas` y se revisó la estructura de cada archivo usando:

`.head()`
`.shape`
`.info()`
Esto para identificar columnas, tipos de datos, número de registros y posibles problemas iniciales.

2. Identificación de problemas de calidad
Se revisaron valores nulos, sentinels y datos inconsistentes.

Se crearon nuevas métricas creadas:

cant_mensajes: cantidad total de mensajes
cant_llamadas: cantidad total de llamadas
cant_minutos_llamada: total de minutos de llamada
Después, esta tabla se combinó con `users_latam.csv` usando un join para crear una tabla `llamada user_profile`.

5. Visualización de distribuciones y detección de outliers
Se creaton histogramas y boxplots para verificar algunos datos y checar outliners:

También se usó el método IQR para detectar valores atípicos.

6. Segmentación de clientes
Se crearon dos segmentaciones principales.

Segmentación por uso y por edad

La mayoría de los usuarios se concentra en el grupo Adulto, seguido de Adulto Mayor y Joven.

7. Insight ejecutivo
Se redactaron conclusiones del negocio y algunas Recomendaciones.

## 📂 Contenido del repositorio

- `notebooks/Sprint 7- Connectatel Data Analisys.ipynb`
  → Notebook principal con limpieza, EDA, distribuciones, outliers y conclusiones.

## ▶ Cómo abrir el notebook en Github

1. Abre el archivo `.ipynb` en GitHub
2. Haz clic en **Open in Colab**

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/Sprint 7- Connectatel Data Analisys.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/` o desde un enlace público (según corresponda)

## 🧠 Objetivo del análisis

- Identificar problemas de calidad de datos
- Construir un pipeline de limpieza reproducible
- Analizar comportamientos, distribuciones y outliers
- Generar insights para el equipo de Estrategia e Integración de EverPeak
