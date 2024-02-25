# Online Prediction

This directory contains all the notebooks related to the online (real-time) prediction service offered by Vertex AI, and how to use it to deploy 🤗 HuggingFace models from the Hub.

For more information on Vertex AI please check [Google Cloud - Vertex AI](https://cloud.google.com/vertex-ai).

## Contents

### Initial guides

* [`01-build-custom-inference-images.ipynb`](./01-build-custom-inference-images.ipynb): contains the steps to build custom prediction containers to run inference on HuggingFace models using 🤗 `transformers.pipeline` for both CPU and GPU, and how to push those to the Google Cloud Container Registry.

* [`02-upload-register-and-deploy-models.ipynb`](./02-upload-register-and-deploy-models.ipynb): contains the steps to upload, register and deploy any model from the HuggingFace Hub in Vertex AI, covering both CPU-only and GPU accelerated inference.

### End-to-end guides (recommended)

* [`03-from-hub-to-vertex-ai.ipynb`](./03-from-hub-to-vertex-ai.ipynb): contains a complete guide to define a custom container for HuggingFace's models and how to upload, register and deploy those in Vertex AI, also including how to use those endpoints for online predictions.

* [`04-from-hub-to-vertex-ai-gpu.ipynb`](./04-from-hub-to-vertex-ai-gpu.ipynb): contains a complete guide to define a custom container for HuggingFace's models and how to upload, register and deploy those in Vertex AI, also including how to use those endpoints for online predictions, but using GPU accelerated inference.

