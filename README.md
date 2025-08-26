# ⚽ Expected Goals (xG) Model with Machine Learning

Este proyecto tiene como objetivo **desarrollar y evaluar un modelo de Machine Learning para calcular la probabilidad de que un tiro termine en gol (Expected Goals, xG)** utilizando datos abiertos de **StatsBomb**.

---

## 📊 Flujo del Proyecto

1. **Obtención de Datos**
   - Se utilizan datos públicos de StatsBomb correspondientes a competiciones de fútbol de élite
   - Los datos incluyen información detallada de cada tiro: coordenadas, tipo de tiro, parte del cuerpo, situación del juego, entre otros

2. **Preprocesamiento**
   - Limpieza de datos y normalización de variables.
   - Transformación de variables categóricas a numéricas mediante técnicas como *one-hot encoding*
   - Conversión de coordenadas en nuevas variables (distancia y ángulo de tiro)
   - Manejo de valores nulos y ajuste de formatos

3. **Análisis Exploratorio de Datos (EDA)**
   - Distribución de tiros y goles según distancia y ángulo
   - Impacto de variables contextuales (parte del cuerpo, asistencia previa, tipo de jugada)
   - Identificación de correlaciones y patrones relevantes para el modelado

4. **Pipeline de Machine Learning**
   - Se desarrolla un **pipeline escalable y reproducible** con scikit-learn.
   - Incluye pasos de:
     - Selección de features.
     - Escalado y transformación.
     - Entrenamiento y validación de modelos.

5. **Modelos Probados**
   - **Regresión Logística**
   - **Random Forest**
   - **CatBoost**
   - **XGBoost**
   - **Linear Discriminant Analysis (LDA)**

6. **Evaluación de Modelos**
   - Métricas utilizadas:
     - **Accuracy**
     - **Precision**
     - **Recall**
     - **F1 Score**
     - **ROC-AUC**
     - **RMSE**
     - **Correlación con el modelo de Statsbomb**
   - Estudio comparativo de desempeño en el **set de entrenamiento**
   - Validación en el **set de test** con predicciones finales

---

## 📈 Resultados

- La **regresión logística** funciona como modelo base, con un buen balance entre interpretabilidad y rendimiento
- **XGBoost y CatBoost** ofrecen mejoras en métricas como ROC-AUC y Brier Score, mostrando mayor capacidad para capturar relaciones no lineales  
- El análisis muestra cómo el xG puede ser un **indicador robusto del rendimiento ofensivo de un equipo o jugador**

---

## 🛠️ Tecnologías Utilizadas

- **Python 3.10+**
- **pandas**, **numpy** → Manipulación de datos
- **matplotlib**, **seaborn** → Visualización
- **scikit-learn** → Preprocesado, pipelines, regresión logística, LDA, Random Forest
- **xgboost**, **catboost** → Gradient Boosting avanzado
- **StatsBombPy** → Acceso a datos de StatsBomb

---

## 🚀 Próximos Pasos

- Incluir métricas de calibración adicionales
- Aplicar validación cruzada estratificada
- Explorar técnicas de *feature engineering* más avanzadas (ej. expected assists, presión rival)
- Desplegar el modelo en una API para consulta en tiempo real

---

## 📬 Autor

Proyecto desarrollado por **Joaquín Loaces**  
Licenciado en Ciencia de Datos - Proyecto personal aplicado al fútbol  
