# Análisis de Clientes y Consumo — ConnectaTel

## 🎯 Objetivo del Proyecto
Analizar el comportamiento de uso de servicios de telecomunicaciones (llamadas, minutos y mensajes) y variables demográficas de los clientes de ConnectaTel (2024), con el propósito de identificar patrones de consumo, evaluar la distribución entre planes (Básico vs. Premium), detectar valores atípicos (*heavy users*) y proponer recomendaciones estratégicas para optimizar la oferta comercial.

---

## 📁 Datasets Utilizados
* **users / Perfiles de usuario:** Datos demográficos del cliente (`user_id`, `age`, `plan`).
* **Registros de consumo:** Métricas agregadas por usuario:
  * `cant_mensajes`: Cantidad total de mensajes enviados.
  * `cant_llamadas`: Número de llamadas realizadas.
  * `cant_minutos_llamada`: Total de minutos consumidos en llamadas.

---

## 🛠️ Etapas del Análisis
1. **Limpieza y Consolidación de Datos:**
   * Unión de tablas por `user_id`.
   * Tratamiento de inconsistencias y valores faltantes en demografía (`age`).
2. **Análisis Exploratorio de Datos (EDA):**
   * Gráficos de distribución (histogramas y KDE) para evaluar el sesgo positivo en variables de uso.
   * Comparación de consumo según el tipo de plan contratado.
3. **Detección y Tratamiento de Outliers:**
   * Identificación visual mediante diagramas de caja (*boxplots*).
   * Cálculo de límites por rango intercuartílico (IQR).
   * Justificación de negocio para conservar a los usuarios intensivos (*heavy users*).
4. **Segmentación de Clientes:**
   * Creación de grupos de uso (`Bajo uso`, `Uso medio`, `Alto uso`) y cohortes de edad.
   * Visualización de distribución de segmentos con `seaborn`.
5. **Síntesis Ejecutiva:**
   * Conclusiones de negocio sobre la homogeneidad de consumo entre planes y recomendaciones de empaquetamiento tarifario.

---

## 🚀 Cómo Ejecutar el Proyecto

### Opción 1: Google Colab
1. Sube el archivo `.ipynb` en [colab.research.google.com](https://colab.research.google.com).
2. Asegúrate de tener los archivos `.csv` en la raíz del entorno o enlazados a Google Drive.
3. Ejecuta todas las celdas en orden: **Runtime** $\rightarrow$ **Run all** (Entorno de ejecución $\rightarrow$ Ejecutar todas).

### Opción 2: Entorno Local (Jupyter Notebook / VS Code)
1. Clona el repositorio:
   ```bash
   git clone [https://github.com/estebanJ2000/sprint7-connectatel.git](https://github.com/estebanJ2000/sprint7-connectatel.git)
   cd sprint7-connectatel
