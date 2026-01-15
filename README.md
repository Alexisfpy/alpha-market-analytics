# Alpha Market Analytics

![Python Version](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

## Descripción General

**Alpha Market Analytics** es una herramienta de análisis financiero cuantitativo diseñada para extraer, procesar y visualizar datos de mercado en tiempo real e históricos utilizando la API de **Alpha Vantage**.

El objetivo de este proyecto es identificar patrones de comportamiento en activos volátiles (como TSLA) mediante el cálculo de indicadores técnicos y análisis estadístico, sirviendo como base para estrategias de trading algorítmico.

## Características Principales

* **Ingesta de Datos:** Conexión robusta con la API de Alpha Vantage (Series temporales diarias/intradía).
* **Procesamiento ETL:** Limpieza y estructuración de datos JSON a DataFrames de Pandas optimizados.
* **Análisis Técnico:** Cálculo automatizado de indicadores clave (SMA, EMA, RSI, MACD).
* **Visualización:** Generación de gráficos interactivos para la interpretación de tendencias.

## Stack Tecnológico

* **Lenguaje:** Python 3.x
* **Data Analysis:** Pandas, NumPy
* **Visualización:** Matplotlib / Seaborn / Plotly
* **API:** Alpha Vantage
* **Gestión de Entorno:** Python-dotenv (para seguridad de credenciales)

## Arquitectura del Proyecto

El flujo de datos sigue una lógica modular para asegurar la escalabilidad:

```mermaid
graph LR
A[Alpha Vantage API] -->|JSON Raw| B(Data Ingestion Module)
B -->|Cleaning| C{Data Processing Core}
C -->|Calculations| D[Technical Indicators]
D -->|Output| E[Visualizations & Reports]
