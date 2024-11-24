### **README para el Proyecto Predictivo de Averías en Aeronaves**

# **Proyecto Machine Learning para The Bridge**

=====================================
# **Modelo Predictivo de Averías en Aeronaves**
Este proyecto utiliza técnicas de Machine Learning para predecir averías en aeronaves, optimizando el mantenimiento preventivo y mejorando la eficiencia operativa. El modelo desarrollado permite reducir costos operativos, minimizar riesgos de seguridad y gestionar de manera proactiva las operaciones aeronáuticas.

---

## **Objetivo**
Predecir averías en aeronaves a partir de datos operativos como retrasos, estaciones, franjas horarias y características de vuelo. El objetivo principal es optimizar los recursos de mantenimiento y evitar fallos no planificados.

---

## **Contenido del Repositorio**
### Estructura de Carpetas:
```
src/
├── data/
│   ├── raw/                # Datos originales sin procesar
│   ├── processed/          # Datos tratados para su uso en el modelo
├── notebooks/
│   ├── TratamientoDatos.ipynb  # Notebook de limpieza y preparación de datos
│   ├── MiniEDA.ipynb           # Análisis Exploratorio de Datos
│   ├── Modelado.ipynb          # Entrenamiento y evaluación de modelos
├── utils/                # Funciones auxiliares utilizadas en el proyecto
├── model/
│   ├── best_rf_model.pkl       # Modelo final entrenado
├── dashboard/
│   ├── dashboard.py            # Dashboard interactivo desarrollado con Streamlit
README.md
```

---

## **Datos Utilizados**
- **Descripción:** Información histórica de vuelos, incluyendo tiempos de retraso, estaciones, franjas horarias y registro de averías.
- **Volumen:** Más de 200,000 registros operativos.
- **Variables Clave:**
  - `Minutos`: Tiempo de retraso en minutos.
  - `Estación`: Ubicación de la aeronave.
  - `Franja_Horaria`: Período del día (mañana, tarde, noche).
  - `ATA`: Variable objetivo que indica si hubo avería (1) o no (0).

---

## **Desarrollo del Proyecto**
### **1. Preparación de los Datos**
- Eliminación de duplicados y valores atípicos.
- Imputación de valores faltantes.
- Creación de nuevas variables como "Franja Horaria" y "Estación del Año".

### **2. Análisis Exploratorio**
- Identificación de estaciones con más averías.
- Relación entre retrasos y probabilidad de fallo.
- Tendencias de averías a lo largo del tiempo.
- Distribución de vuelos entre averías.

### **3. Modelado**
- Modelos probados:
  - Logistic Regression.
  - Random Forest.
  - Gradient Boosting.
- **Modelo seleccionado:** Random Forest con optimización de hiperparámetros usando GridSearchCV.
- Métricas clave:
  - **ROC-AUC:** 0.9828.
  - **Precisión general:** 98.3%.
  - **Falsos positivos:** 0.
  - **Falsos negativos:** ~3%.

### **4. Resultados**
- Precisión y recall altos para la clase `1` (avería).
- Impacto directo en la planificación del mantenimiento preventivo y reducción de costos.

---

## **Dashboard**
Un dashboard interactivo fue desarrollado con Streamlit para:
- Visualizar las métricas clave del modelo.
- Analizar la curva ROC y la matriz de confusión.
- Explorar la distribución de probabilidades de predicción.

---

## **Conclusiones**
1. El modelo tiene un alto rendimiento con un **ROC-AUC de 0.9828**.
2. Detecta el 97% de las averías reales, lo que permite prevenir fallos críticos.
3. Reducción de falsos positivos evita alertas innecesarias y ahorra recursos.
4. Se proponen futuras mejoras con datos adicionales (clima, mantenimiento, etc.).

---

## **Méjoras a implementar para un modelo más óptimo**
1. Incorporar datos adicionales como condiciones climáticas y historial de mantenimiento.
2. Ajustar umbrales de decisión para reducir falsos negativos.
3. Implementar el modelo en un entorno de producción y evaluar su impacto.

---

## **Tecnologías Utilizadas**
- **Lenguaje:** Python.
- **Bibliotecas:** Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, Streamlit.
- **Herramientas:** Jupyter Notebook, Git, PowerPoint.

---

## **Autor**
- [Víctor Caballero Cañamero] - Data Scientist en formación en The Bridge.
- LinkedIn: [Víctor Caballero - Analista de Operativa de Mantenimiento](https://www.linkedin.com/in/v-c-c/)
- GitHub: [VictorCC-Repo](https://github.com/VictorCC-Repo)
```
