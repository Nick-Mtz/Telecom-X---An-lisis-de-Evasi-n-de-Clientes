# 📊 Telecom X – Customer Churn Analysis  

Este proyecto forma parte de un desafío de análisis de datos en el sector de **telecomunicaciones**, con el objetivo de comprender los factores que llevan a la **evasión de clientes (churn)**.  

La empresa **Telecom X** enfrenta una alta tasa de cancelaciones (~26%) y necesita identificar patrones de comportamiento para diseñar **estrategias de retención** y preparar el terreno para modelos predictivos de Machine Learning.  

---

## 📝 Objetivo  
El objetivo del análisis es:  
- Comprender la **magnitud y distribución del churn**.  
- Identificar **variables críticas** relacionadas con la evasión (contrato, método de pago, tenure, gasto).  
- Obtener **insights accionables** que sirvan de base para estrategias de negocio y futuros modelos de predicción.  

---

## 🗂️ Estructura del repositorio  
📂 TelecomX-Churn
├── 📄 TelecomX_Data.json # Dataset original en formato JSON
├── 📄 TelecomX_diccionario.md # Diccionario de datos con descripción de variables
├── 📓 TelecomX_Analysis.ipynb # Notebook principal con ETL, EDA y visualizaciones
└── README.md # Este archivo


---

## 📚 Tecnologías utilizadas  
- [Python 3](https://www.python.org/)  
- [Pandas](https://pandas.pydata.org/)  
- [Matplotlib](https://matplotlib.org/)  
- [Seaborn](https://seaborn.pydata.org/)  

---

## 📊 Análisis realizado  

1. **ETL y exploración de datos**  
   - Normalización del JSON con `pandas.json_normalize`.  
   - Conversión de tipos (ej: `TotalCharges` de texto a numérico).  
   - Limpieza de inconsistencias y creación de columna `Cuentas_Diarias`.  

2. **Análisis descriptivo**  
   - Media, mediana, desviación estándar de tenure, monthly charges y total charges.  
   - Identificación de alta dispersión entre clientes de corto y largo plazo.  

3. **Distribución de churn**  
   - Clientes activos: **~71%**  
   - Clientes que cancelaron: **~26%**  
   - Inconsistencias menores: ~3%  

4. **Churn por variables categóricas**  
   - **Mayor churn**: contratos `Month-to-month` y método de pago `Electronic check`.  
   - **Menor churn**: contratos `One year` / `Two year`.  
   - Género: diferencias no significativas.  

5. **Churn por variables numéricas**  
   - **Baja antigüedad (tenure < 1 año)** correlaciona con mayor churn.  
   - Clientes con **bajo gasto acumulado** tienden a cancelar más rápido.  

---

## ✅ Hallazgos principales  

- Los **contratos mensuales** y el **método de pago `Electronic check`** son los principales impulsores de la evasión.  
- Los clientes que se van lo hacen **temprano en la relación** (tenure bajo).  
- El **riesgo de churn disminuye significativamente en contratos de mayor plazo**.  

---

## 💡 Recomendaciones  

1. **Retención temprana**: enfocar beneficios en los primeros 6 meses.  
2. **Incentivar contratos largos** con descuentos o promociones.  
3. **Migrar clientes** de `Electronic check` a métodos automáticos más seguros.  
4. **Alertas tempranas** combinando tenure bajo + electronic check + monthly alto.  
5. **Bundles de valor** (servicios de seguridad y streaming) para aumentar permanencia.  

---

👤 Autor

Nick Martinez

LinkedIn: www.linkedin.com/in/ccarloss


   
