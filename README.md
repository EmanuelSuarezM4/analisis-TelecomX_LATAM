# Análisis de Evasión de Clientes — Telecom X

## Propósito del Análisis
El propósito de este proyecto es identificar los factores críticos que influyen en la **evasión de clientes (churn)** en la empresa Telecom X. A través de un análisis detallado de datos demográficos, financieros y de servicios, buscamos proporcionar recomendaciones estratégicas que permitan reducir la tasa de abandono y mejorar la retención de usuarios en etapas críticas de su ciclo de vida.

---

## Estructura del Proyecto
El proyecto se desarrolló íntegramente en un notebook de Python (Jupyter/Google Colab) y se organiza en las siguientes secciones técnicas:

1.  **Limpieza y Tratamiento de Datos:**
    * Normalización de estructuras anidadas y aplanamiento de datos.
    * Eliminación de **11 registros** con valores incoherentes en `Cargos_Totales`.
    * Traducción y estandarización de columnas para asegurar la claridad en el reporte.
    * Ingeniería de variables: creación de la métrica `Cuentas_Diarias` y `Cant_Servicios`.
2.  **Análisis Descriptivo (EDA):**
    * Cálculo de métricas de tendencia central (media, mediana) y dispersión.
    * Visualización de la proporción de clientes que permanecieron frente a los que se dieron de baja.
3.  **Análisis de Indicadores:**
    * Distribución de evasión por variables categóricas como Género, Contrato y Método de Pago.
    * Análisis del impacto de variables numéricas como el tiempo de contrato (antigüedad) y cargos mensuales.
4.  **Análisis de Correlación (Extra):**
    * Cálculo de la matriz de correlación para identificar los predictores con mayor peso matemático en la evasión.
5.  **Informe Final:**
    * Síntesis de hallazgos y recomendaciones estratégicas para la toma de decisiones.

---

## Ejemplos de Gráficos e Insights
A continuación, se presentan las visualizaciones clave que sustentan el análisis:

<img width="663" height="516" alt="image" src="https://github.com/user-attachments/assets/8ee87eee-c25d-422e-b77a-76fcd58fa643" />

<img width="1025" height="1482" alt="image" src="https://github.com/user-attachments/assets/503bdd47-98a6-4e44-af96-be5dafb567bd" />


### Principales Insights:
* **Factor Contrato:** Los clientes con contrato **"Month-to-month"** presentan el mayor nivel de riesgo de evasión.
* **Ventana Crítica:** La mayoría de las deserciones ocurren en los primeros meses de antigüedad; los clientes con mayor permanencia tienden a ser más estables.
* **Método de Pago:** El uso de **"Electronic check"** está asociado a una tasa de fuga significativamente superior a los métodos automáticos.
* **Sensibilidad al Precio:** Se observa que los clientes con cargos mensuales más altos tienen una mayor densidad de evasión.

<img width="1321" height="558" alt="image" src="https://github.com/user-attachments/assets/db87875f-88f9-4570-bf53-e31e41dde1f4" />

### Recomendación Estratégica:
Incentivar la migración de contratos mensuales a anuales y fortalecer el seguimiento de servicio durante los primeros 6 meses de antigüedad para reducir la deserción temprana.

<img width="1341" height="1020" alt="image" src="https://github.com/user-attachments/assets/ab56a47e-6ab1-4818-81fb-81b1a3ae0fbb" />

---

## Instrucciones para Ejecutar el Notebook

### Requisitos
Para ejecutar este análisis, asegúrate de tener instalado:
* Python 3.10+
* Google Colab (recomendado) o Jupyter Notebook.

### Bibliotecas Necesarias
Puedes instalar las dependencias ejecutando:
```bash
pip install pandas matplotlib seaborn numpy
