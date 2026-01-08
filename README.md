📊 Desafío: Análisis de Evasión de Clientes — Telecom X

![Estado del Proyecto](https://img.shields.io/badge/Estado-Finalizado-success)
![Tecnologías](https://img.shields.io/badge/Tecnolog%C3%ADas-Python%20%7C%20Pandas%20%7C%20Matplotlib-blue)

---

## 🎯 1. Objetivo del Proyecto

Telecom X enfrenta una alta tasa de cancelaciones y necesita identificar los factores que impulsan la evasión (_churn_). El objetivo es realizar un **ETL y análisis exploratorio** para:

- Entender el patrón de abandono de clientes.
- Identificar variables asociadas a mayor riesgo de churn (contrato, servicio de internet, método de pago, antigüedad, cargos).
- Generar insights accionables para estrategias de retención.

**Indicadores evaluados:**

1. **Tasa de churn** → Porcentajes y conteos.
2. **Cargos mensuales y total acumulado** → Sensibilidad al precio.
3. **Tipo de contrato** → Riesgo según compromiso (mensual vs anual).
4. **Servicios contratados** (soporte, seguridad, streaming) → Percepción de valor.
5. **Antigüedad (tenure)** → Riesgo por etapa del ciclo de vida.

---

## 🛠️ 2. Estructura y Tecnologías

El análisis está implementado en un notebook (`ca_telecom_x.ipynb`) diseñado para ejecutarse localmente (Jupyter / VS Code) o en entornos gestionados.

### 2.1. Tecnologías Utilizadas

|     Librería     | Propósito                                                    |
| :--------------: | :----------------------------------------------------------- |
|   **`pandas`**   | Carga y transformación de datos (ETL)                        |
| **`matplotlib`** | Visualizaciones estáticas (gráficas de barras, distribución) |
|  **`jupyter`**   | Ejecución interactiva del notebook                           |

### 2.2. Archivos Clave

- `ca_telecom_x.ipynb`: Notebook principal con ETL, análisis y conclusiones.
- `requirements.txt`: Dependencias del proyecto.
- `evasion_clientes.png`: Figura generada de la distribución de churn (se crea al ejecutar la celda correspondiente).
- `.gitignore`: Reglas para evitar subir entornos y archivos temporales.

---

## 📈 3. Visualizaciones Clave

|  Nº   | Gráfico                         | Título                                                           | Métrica Clave                            |
| :---: | :------------------------------ | :--------------------------------------------------------------- | :--------------------------------------- |
| **1** | Distribución de churn           | **Crisis de Retención: 1 de cada 4 clientes abandona**           | Conteo y % de `churn`                    |
| **2** | Churn por variables categóricas | **Evasión por `internet_service`, `contract`, `payment_method`** | Tasa de churn por categoría              |
| **3** | Segmentación por cargos         | **Impacto de `charges_monthly` y `charges_total`**               | Churn por cuartiles (qcut)               |
| **4** | Antigüedad del cliente          | **Riesgo por `tenure` (Nuevo → Muy leal)**                       | Churn por tramos de tiempo               |
| **5** | Tablas resumen                  | **Crosstabs y estadísticas descriptivas**                        | Soporte para hipótesis y recomendaciones |

Cada gráfico está acompañado de crosstabs y comentarios interpretativos en el notebook para facilitar la lectura.

---

## ⚙️ 4. Ejecución y Dependencias

### 4.1. Ejecución Local (Windows PowerShell)

1. Crear y activar el entorno virtual:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

2. Instalar dependencias:

```powershell
pip install -r requirements.txt
```

3. Abrir `ca_telecom_x.ipynb` en Jupyter o en VS Code y ejecutar las celdas en orden. La primera celda incluye una verificación rápida del entorno (versiones de `pandas`, `matplotlib`, `jupyter`).

### 4.2. Notas sobre reproducibilidad

- Para mayor reproducibilidad, se recomienda fijar versiones en `requirements.txt` (puedo generarlas si quieres).
- El dataset se descarga desde una URL pública definida en el notebook; asegúrate de tener conexión para la extracción.

---

## 📊 5. Conclusiones e Insights (resumen)

- Aproximadamente **26–27%** de los clientes analizados se dieron de baja (1 de cada 4).
- **Tipo de contrato:** clientes en contratos **mensuales** presentan la mayor probabilidad de churn.
- **Servicio de Internet:** usuarios de **fibra óptica** muestran tasas de evasión superiores (posible expectativa no cumplida).
- **Método de pago:** pagos manuales como `Electronic check` se asocian a mayor churn.
- **Servicios adicionales** (soporte, seguridad, protección de dispositivos) reducen significativamente la evasión.
- **Antigüedad y cargos:** clientes nuevos y con cargos mensuales altos o bajo gasto acumulado concentran el mayor riesgo.

### ✅ Recomendaciones ejecutivas

1. **Foco en retención temprana:** programas de onboarding y seguimiento para clientes nuevos.
2. **Incentivos por compromiso:** ofertas para migrar de contratos mensuales a anuales.
3. **Mejoras en servicios premium:** evaluar calidad y soporte de fibra óptica.
4. **Promocionar pagos automáticos:** reducir fricción y riesgo de abandono.
5. **Ofrecer paquetes con servicios adicionales** para aumentar percepción de valor.

---

## 🤝 6. Autoría

Proyecto desarrollado por **Telecom X – Equipo de Análisis** (notebook preparado por el autor del repositorio).

Si quieres que fije versiones en `requirements.txt`, organice las figuras en una carpeta `figures/` o haga un commit y push automático, dime cuál prefieres y lo implemento.
