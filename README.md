**Detección de Fraude en Transacciones con Autoencoders: Proyecto realizado en la materia Deep Learning**

**Descripción del Proyecto**
Este proyecto implementa un Autoencoder (aprendizaje no supervisado) para detectar transacciones fraudulentas en un dataset de tarjetas de crédito. El dataset consta de:
- 28 features codificadas (por confidencialidad de datos sensibles).
- Amount: Monto de la transacción.
- Class: Variable binaria que indica si la transacción es fraudulenta o no.

**Problemática**
El dataset está altamente desbalanceado:
- 99.8% de las transacciones son normales.
- 0.2% corresponden a fraudes.

Ante este desbalanceo, los modelos supervisados tradicionales suelen sobreajustarse a la clase mayoritaria. Es por esto que se optó por un Autoencoder, que aprende a reconstruir transacciones normales y detecta fraudes mediante un alto error de reconstrucción, ya que las transacciones fraudulentas, al ser atípicas, no se reconstruyen bien.

**Técnicas Implementadas**
Preprocesamiento: Normalización de features (ej. Amount) y manejo de datos desbalanceados.

Modelado: Entrenamiento de un Autoencoder en Keras para aprender patrones de transacciones legítimas.

Detección de anomalías: Cálculo del MSE (Error Cuadrático Medio) para identificar transacciones con errores de reconstrucción inusualmente altos (potenciales fraudes).

Evaluación: Métricas como precisión, recall y matriz de confusion en el conjunto de test.

**Herramientas**
- Pandas, NumPy, Scikit-learn.
- TensorFlow/Keras para el Autoencoder.
- Matplotlib/Seaborn para visualización.
