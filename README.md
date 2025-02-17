# Engineering_of_ML
This repository consists of various Assignments that I have completed using MLflow, Evidently, Kubeflow and Deepchecks
- **MLflow**: MLflow is an open-source platform for managing the machine learning (ML) lifecycle, developed by Databricks. It helps track, reproduce, and deploy ML models efficiently.
- **Great Expectations**: Data Validation
- **Evidently AI**: Automate ML monitoring (can associate with mlflow), Handle data drift(feature drift, target drift, model performance monitoring)
- **Optuna, Ray tune (python libraries)**: Automatic Hyperparameter optimization Framework, has TPE sampler(bayesian))
- **KServe** : KServe is an open-source model serving platform for deploying and managing machine learning (ML) models in Kubernetes environments. It is designed to provide serverless, scalable, and production-ready model inference while simplifying ML model deployment.
- **MLServer** :🔹 Purpose: MLServer is a high-performance model inference server, designed for production-ready ML model serving.
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

### End-to-End Pipeline: MLflow → MLServer → KServe 🚀
This is a step-by-step process for building a model deployment pipeline starting from MLflow (for model training and logging), serving with MLServer (for model inference), and deploying at scale with KServe (Kubernetes-based model serving). 
Step-by-Step Process
1️⃣ Train & Save Model in MLflow
First, you'll train a model and log it into MLflow, which is the central repository for model tracking and versioning.
- The model is now saved in MLflow and is accessible via its URI (e.g., runs:/<run_id>/model)
2️⃣ Export the MLflow Model
You can serve the saved model directly using MLServer, which supports models stored in MLflow.
3️⃣ Serve MLflow Model with MLServer
MLServer is used to serve the model saved in MLflow.
Install MLServer with MLflow Support : pip install mlserver mlserver-mlflow
# Create the model-settings.json File for MLServer
Define how MLServer should load the MLflow model by creating a model-settings.json configuration file.
4️⃣ Deploy the MLServer-Served Model Using KServe
After serving the model with MLServer, you can deploy it using KServe to handle scaling and manage the model lifecycle in a Kubernetes cluster.
Prepare the KServe InferenceService YAML, KServe uses the InferenceService resource to manage machine learning model deployments in Kubernetes.
# Create a YAML file that defines the deployment of your model using KServe.
-The modelUri points to the MLflow model stored in your artifact store.
- Adjust resources as needed based on your deployment.
- Deploy the Model with KServe
- To deploy this YAML file to a Kubernetes cluster with KServe.
5️⃣ Predict with the KServe-Served Model
Once the model is deployed using KServe, you can send a request to the exposed API.
Send Prediction Request via cURL. After KServe has deployed the model, you can send predictions to it using cURL.

🔄 Summary of the Pipeline

- Train and save the model using MLflow
- Serve model using MLServer
- Deploy model with KServe for scalable, Kubernetes-based serving
- Send predictions via API to KServe

-------------------------------------------------------------------------------------------------------------------------------------------------
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
