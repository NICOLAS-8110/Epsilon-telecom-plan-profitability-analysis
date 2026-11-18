<img width="1280" height="640" alt="WhatsApp Image 2026-11-17 at 3 00 46 PM (4)" src="https://github.com/user-attachments/assets/fa1c5351-3f8c-4acd-97a4-e29fc052c957" />

# 📱 Análisis de Rentabilidad de Planes de Telecomunicaciones (Megaline)

## 📋 Descripción
**Megaline** es una compañía de telecomunicaciones que ofrece a sus clientes dos planes de prepago: **Surf** y **Ultimate**. El objetivo de este proyecto fue analizar el comportamiento de consumo de los usuarios durante 2018 para determinar cuál de los dos planes genera mayores ingresos para la empresa.

Para ello, se procesaron registros de llamadas, mensajes de texto y consumo de datos móviles, estimando la facturación mensual por usuario y aplicando pruebas de hipótesis estadísticas para validar si las diferencias financieras entre ambos planes y por región eran estadísticamente significativas.

## 🎯 Objetivos
- ✅ Evaluar la calidad e integridad de los conjuntos de datos operativos.
- ✅ Analizar los patrones de consumo por tipo de servicio (llamadas, SMS e internet).
- ✅ Calcular el uso mensual agregado por cliente y sus excedentes tarifarios.
- ✅ Estimar los ingresos mensuales generados por cada usuario.
- ✅ Comparar el desempeño financiero y la estabilidad de los planes **Surf** y **Ultimate**.
- ✅ Validar mediante pruebas de hipótesis las diferencias de ingresos entre planes y regiones (NY-NJ vs. otras regiones).
- ✅ Formular recomendaciones estratégicas para orientar las campañas comerciales de Megaline.

## 🛠️ Herramientas y Habilidades Utilizadas
* **Lenguaje:** Python
* **Librerías:** Pandas, NumPy, Matplotlib, Seaborn y SciPy
* **Entorno:** Jupyter Notebook
* **Técnicas:** Estadística descriptiva, Pruebas de hipótesis (t-test), Limpieza y consolidación de datos, Cálculo de métricas de negocio y Visualización de datos.

## 📊 Fuente de Datos
El estudio se desarrolló utilizando registros operativos de clientes de Megaline correspondientes al año 2018, distribuidos en cinco tablas relacionales:

* `megaline_users.csv`: Datos demográficos, ciudad/región y plan asignado.
* `megaline_calls.csv`: Registro detallado de llamadas y duración en minutos.
* `megaline_messages.csv`: Historial de mensajes de texto enviados.
* `megaline_internet.csv`: Sesiones y volumen de tráfico de datos móviles (MB).
* `megaline_plans.csv`: Condiciones, límites incluidos y tarifas por excedente de cada plan.

## ⚙️ Metodología
1. **Preparación y saneamiento:** Exploración inicial, revisión de tipos de datos, tratamiento de valores ausentes, detección de duplicados y estandarización de formatos.
2. **Ingeniería de métricas mensuales:** Cálculo por usuario y mes del número de llamadas, minutos redondeados, SMS enviados y GB consumidos, consolidando todo en una tabla maestra.
3. **Modelado de ingresos:** Cálculo de excedentes de minutos, mensajes y datos según las reglas tarifarias de Surf y Ultimate para obtener la facturación mensual exacta por cliente.
4. **Análisis exploratorio (EDA):** Comparación visual y estadística del consumo e ingresos mediante histogramas, gráficos de barras y diagramas de caja (boxplots).
5. **Validación estadística:** Ejecución de pruebas de hipótesis para evaluar diferencias en ingresos promedio entre planes y entre la región NY-NJ frente al resto del país.

## 💡 Principales Hallazgos
* **Consumo de llamadas:** El promedio de minutos fue muy similar en ambos planes; la mayoría de los usuarios se mantuvo por debajo del límite incluido.
* **Consumo de mensajes:** Los clientes de *Ultimate* enviaron más SMS en promedio, aunque en ambos planes el uso estuvo muy lejos de alcanzar el tope tarifario.
* **Consumo de internet:** *Ultimate* registró un tráfico de datos ligeramente superior, pero una gran proporción de usuarios de *Surf* superó su límite incluido, convirtiendo los datos móviles en el principal detonante de cargos extra.
* **Rentabilidad por plan:**
  * **Surf:** Ingreso promedio de **$57.29 USD/mes** (alta variabilidad debido a cobros por excedentes).
  * **Ultimate:** Ingreso promedio de **$72.12 USD/mes** (ingresos superiores y mucho más estables).

## 🧪 Resultados de las Pruebas Estadísticas
* **Comparación de ingresos: Surf vs. Ultimate**
  * **H₀:** Ambos planes generan el mismo ingreso promedio. | **H₁:** Los ingresos promedio son diferentes.
  * **Resultado:** `p-value = 4.88 × 10⁻²⁵` → **Se rechaza H₀.** Existe una diferencia estadísticamente significativa; *Ultimate* genera mayores ingresos.
* **Comparación regional: NY-NJ vs. Otras regiones**
  * **H₀:** Los ingresos promedio son iguales. | **H₁:** Los ingresos promedio son diferentes.
  * **Resultado:** `p-value = 0.0186` → **Se rechaza H₀.** Existe una diferencia significativa en la facturación promedio entre los clientes de NY-NJ y el resto de regiones.

## 📈 Visualizaciones Desarrolladas
* Consumo promedio mensual y distribución de minutos, mensajes y datos móviles por plan.
* Diagramas de caja (boxplots) para identificar dispersión y valores atípicos en llamadas y tráfico de internet.
* Distribución comparativa de ingresos mensuales generados por plan.

## 📂 Archivos Principales
* `Epsilon_telecom_plan_profitability_analysis.ipynb`
* `megaline_calls.csv`
* `megaline_internet.csv`
* `megaline_messages.csv`
* `megaline_plans.csv`
* `megaline_users.csv`

## 🏁 Conclusión
El análisis demuestra que, aunque los patrones de llamadas y mensajes son similares entre los usuarios de Surf y Ultimate, el consumo de datos móviles y la estructura tarifaria marcan una diferencia sustancial en la facturación. Los clientes de **Ultimate** no solo aportan un ingreso promedio mayor ($72.12 USD frente a $57.29 USD), sino que garantizan un flujo de caja mucho más predecible. Respaldado por las pruebas estadísticas, se recomienda que Megaline enfoque sus esfuerzos comerciales y presupuestos publicitarios en promover el plan **Ultimate** para maximizar su rentabilidad.
