# Análisis de Churn en Clientes de Telecomunicaciones

## 📄 Descripción del Proyecto
Este proyecto tiene como objetivo analizar y predecir el fenómeno de churn (abandono del servicio) en clientes de una compañía de telecomunicaciones.
Se utiliza un dataset tratado con información demográfica, contractual y de consumo de los clientes, para entrenar y evaluar modelos de clasificación capaces de identificar patrones que conduzcan a la cancelación del servicio.

## 📊 Diccionario de Datos

  - customerID: Identificador único de cliente.
  - Churn: Variable objetivo (1 si el cliente canceló, 0 si permaneció).
  - gender: Género del cliente.
  - SeniorCitizen: Si el cliente tiene 65 años o más.
  - Partner: Indica si el cliente tiene pareja.
  - Dependents: Indica si el cliente tiene dependientes.
  - tenure: Meses de permanencia en la compañía.
  - PhoneService: Suscripción a servicio telefónico.
  - MultipleLines: Más de una línea telefónica.
  - InternetService: Tipo de servicio de internet.
  - OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies: Servicios adicionales.
  - Contract: Tipo de contrato.
  - PaperlessBilling: Facturación electrónica.
  - PaymentMethod: Método de pago.
  - Charges.Monthly: Cargos mensuales.
  - Charges.Total: Cargos totales acumulados.

## 🔍 Metodología

1. Preprocesamiento de datos
   - Eliminación de columnas irrelevantes.
   - Conversión de variables booleanas a enteros.
   - Reemplazo de valores categóricos por numéricos.
   - Normalización de variables continuas.
   - Codificación One-Hot Encoding para variables categóricas.

2. Análisis exploratorio
  - Evaluación de la proporción de churn.
  - Análisis de correlación global y dirigido.
  - Identificación de variables más influyentes.

3. Modelado
  - Entrenamiento inicial sin balanceo de clases usando LazyPredict.
  - Selección de dos modelos con alto Recall:
     - LogisticRegression
     - LinearSVC
  - Uso de K-Fold Cross Validation con Recall como métrica principal.
  - Implementación de NearMiss para balanceo de clases.
  - Comparación de resultados con y sin balanceo.

4. Interpretación
   - Extracción de coeficientes para identificar la importancia de las variables.
   - Conclusiones sobre las características que más influyen en el churn.

## 📈 Principales Hallazgos
   - El 27% de los clientes han cancelado el servicio.
   - Variables que aumentan la probabilidad de churn:
     - Contrato mes a mes.
     - Internet por fibra óptica.
     - Pago mediante cheque electrónico.
  - Variables que reducen la probabilidad de churn:
     - Mayor tiempo de permanencia (tenure).
     - Contrato a 2 años.
     - Tener servicio de internet.
  - El Recall fue priorizado como métrica debido a la importancia de identificar a los clientes que probablemente cancelarán.
  - Ambos modelos elegidos (LogisticRegression y LinearSVC) destacan por:
    - Alto rendimiento en Recall.
    - Velocidad de entrenamiento.
    - Facilidad de interpretación de resultados.

## 📂 Archivos
- ChallengeTelecomX2.ipynb: Notebook con todo el análisis, procesamiento y modelado.

## 📬 Contacto
📧 jmesa@gmail.com

**Nota**: Este README fue creado con el apoyo de inteligencia artificial.
✍️ Asistente IA: GPT-5 Helper
