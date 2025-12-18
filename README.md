# 🏨 Predicción de Precios de Airbnb en Madrid (End-to-End ML Project)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Khn3QrZ9Q-YAK2P7iDfoa1dYjcGNkeal?usp=sharing)

> **Proyecto de Data Science y Econometría Urbana** aplicado al mercado inmobiliario de Madrid.

## 📋 Descripción del Proyecto
Este proyecto analiza los determinantes del precio de alquiler turístico en Madrid utilizando un dataset de 15,000 inmuebles. El objetivo fue superar las limitaciones de los modelos lineales tradicionales mediante algoritmos de Machine Learning, logrando predecir el valor de mercado con mayor precisión.

## 🛠️ Tecnologías Utilizadas
* **Python 3.10**
* **Data Processing:** Pandas, NumPy.
* **Visualization:** Seaborn, Matplotlib.
* **Econometrics:** Statsmodels (OLS).
* **Machine Learning:** Scikit-Learn (Random Forest), XGBoost.
* **Hyperparameter Tuning:** RandomizedSearchCV.

## 📊 Metodología
1.  **Limpieza de Datos:** Tratamiento de outliers y nulos.
2.  **Feature Engineering:**
    * Creación de métrica espacial con **Fórmula Haversine** (Distancia a Puerta del Sol).
    * Transformación logarítmica del precio (`log_price`) para normalizar la distribución.
3.  **Modelado:** Comparación de 3 enfoques (OLS vs Random Forest vs XGBoost).

## 🏆 Resultados: La Batalla de Modelos
El modelo **XGBoost** resultó ganador, mejorando la capacidad predictiva en un **15%** respecto al modelo econométrico base.

| Modelo | R² Score | Interpretación |
| :--- | :--- | :--- |
| **Regresión Lineal (OLS)** | 0.528 | Base de referencia. Captura tendencias lineales. |
| **Random Forest** | 0.670 | Gran mejora. Captura no-linealidades. |
| **XGBoost (Optimizado)** | **0.675** | **Modelo Ganador.** Máxima precisión tras ajuste de hiperparámetros. |

## 💡 Conclusiones Económicas (Key Drivers)
El análisis de importancia de variables reveló qué valora realmente el mercado:
1.  **Privacidad:** El tipo de habitación (Privada/Compartida vs Casa Entera) es el factor #1.
2.  **Capacidad:** El número de personas que caben (`accommodates`) pesa más que los metros cuadrados o baños.
3.  **Ubicación:** Se validó la hipótesis de *Alonso-Muth-Mills*: el precio cae significativamente al alejarse del Km 0.

---
### 🚀 Cómo ejecutar este proyecto
Puedes visualizar y ejecutar el código directamente en la nube haciendo clic en el botón de **"Open in Colab"** al inicio de este documento.

*Nota: Si descargas el notebook localmente, asegúrate de actualizar la ruta del archivo `listings.csv`.*

**Autor:** Luis Mauricio Aguirre Stornaiuolo
