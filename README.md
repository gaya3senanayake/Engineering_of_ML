# Engineering_of_ML
This repository consists of various Assignments that I have completed using MLflow, Evidently, Kubeflow and Deepchecks
- **MLflow**: MLflow is an open-source platform for managing the machine learning (ML) lifecycle, developed by Databricks. It helps track, reproduce, and deploy ML models efficiently.
- **Great Expectations**: Data Validation
- **Evidently AI**: Automate ML monitoring (can associate with mlflow), Handle data drift(feature drift, target drift, model performance monitoring)
- **Optuna, Ray tune (python libraries)**: Automatic Hyperparameter optimization Framework, has TPE sampler(bayesian))
- **KServe** : KServe is an open-source model serving platform for deploying and managing machine learning (ML) models in Kubernetes environments. It is designed to provide serverless, scalable, and production-ready model inference while simplifying ML model deployment.
- **MLServer** :🔹 Purpose:

MLServer is a high-performance model inference server, designed for production-ready ML model serving.
🔹 Key Features:
✅ Optimized for Inference – Low latency, high scalability.
✅ Multi-Model Support – Can serve multiple models at the same time.
✅ Custom Runtimes – Supports various ML frameworks (e.g., TensorFlow, PyTorch, ONNX, XGBoost).
✅ Kubernetes & KServe Integration – Ideal for cloud-based production deployments.
🔹 How It Works:
MLServer loads models into memory and exposes them as REST or gRPC APIs for inference.
Can be used in Kubernetes-based deployments like KServe.
📌 Best for:
Production-scale model serving (high-performance API for inference).
Deploying multiple models efficiently with lower latency.

## Visualization of Results

Here are some sample images from the dataset:
### Information on the dataset
![Sample 1](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/dataset-info.png)

### MLflow sample view
![Sample 2](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/ass3-example.png)

### MLflow experiement view
![Sample 3](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/mlflow-run.png)

### MLflow run details view
![Sample 4](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/mlflow-run-detail3.png)

### deepchecks compare models details view
![Sample 5](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/deepchecks-compare-models.png)

### deepchecks inference time details view
![Sample 6](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/deepchecks-inference-time.png)

### deepchecks train test performance details view
![Sample 7](https://github.com/gaya3senanayake/Engineering_of_ML/blob/main/Images/deepchecks-train-test-performance.png)
