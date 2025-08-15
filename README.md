**Detección de Fraude en Transacciones con Autoencoders: proyecto realizado en la materia Deep Learning**

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

- Preprocesamiento: Normalización de features (Amount).
- Modelado: Entrenamiento de un Autoencoder en Keras para aprender patrones de transacciones legítimas.
- Detección de anomalías: Cálculo del MSE (Error Cuadrático Medio) para identificar transacciones con errores de reconstrucción inusualmente altos (potenciales fraudes).
- Evaluación: Métricas como precisión, recall y matriz de confusion en el conjunto de test.

**Resultado**

 Se obtuvo un modelo que detecto 91 transacciones fraudulentas (con un total de 98 en el dataset)

**Herramientas**
- Pandas, NumPy, Scikit-learn.
- Keras para el Autoencoder.
- Matplotlib/Seaborn para visualización.

__________________________________________________________________________________________________________________________________________________________________________________________________________________
**Credit Card Fraud Detection with Autoencoders: Project developed for Deep Learning course**

**Project Description**

This project implements an Autoencoder (unsupervised learning) to detect fraudulent transactions in a credit card dataset. The dataset consists of:
- 28 encoded features (due to sensitive data confidentiality).
- Amount: Transaction amount.
- Class: Binary variable indicating whether the transaction is fraudulent (1) or not (0).

**Challenge**

The dataset is highly imbalanced:
- 99.8% of transactions are legitimate.
- 0.2% correspond to fraud.

Because of this imbalance, traditional supervised models tend to overfit the majority class. For this reason, an Autoencoder was chosen to reconstruct normal transactions and detects fraud through high reconstruction error, as fraudulent transactions are poorly reconstructed.

**Implemented Techniques**

- Preprocessing: Feature normalization (Amount).
- Modeling: Training an Autoencoder using Keras to learn patterns from legitimate transactions.
- Anomaly Detection: Calculating MSE (Mean Squared Error) to identify transactions with unusually high reconstruction errors (potential fraud).
- Evaluation: Metrics such as precision, recall, and confusion matrix on the test set.

**Results**

The model successfully detected 91 fraudulent transactions (out of 98 total fraud cases in the dataset).

**Tools**

- Pandas, NumPy, Scikit-learn.
- Keras for the Autoencoder implementation.
- Matplotlib/Seaborn for visualization.

