# Vertex AI 🤝🏻 HuggingFace

Collection of examples on how to train, deploy and monitor 🤗 HuggingFace models in Google Cloud Vertex AI

## Installation

* `gcloud` CLI needs to be installed and logged in the project that will be used. See the installation notes at https://cloud.google.com/sdk/docs/install

* `docker` needs to be installed locally, and up and running, since it will be used to build the CPR images before pushing those to the container registry. See the installation notes at https://docs.docker.com/engine/install/

* `google-cloud-aiplatform` Python library is required to programatically build the CPR image, to define the custom prediction code via a custom `Predictor`, to run the online/batch predictions, etc.

    `pip install google-cloud-aiplatform --upgrade`

* `git lfs` needs to be installed for pulling / cloning models from the HuggingFace Hub. See the installation notes at https://git-lfs.com/.

## Contents

* [`online-prediction/`](./online-prediction): contains some notebooks to explain the different steps to upload, register and deploy any model from the HuggingFace Hub in Vertex AI, covering both CPU-only and GPU accelerated inference.

## What's next?

This collection will be updated iteratively, and here are some of the things that are currently under development and will be published soon:

* [ ] `pipelines/`: contains some notebooks to explain how to build custom pipelines, focusing in fine-tuning of HuggingFace models (which could later be deployed within Vertex AI)
* [ ] `batch-predictions/`: contains some notebooks to explain the concept of batch predictions, comparing those to online predictions, and also providing some practical use cases
* [ ] `real-time-inference/sentence-transformers/`: contains some notebooks explaining how to upload, register and deploy `SentenceTransformers` models in Vertex AI

Additionally, a Python package is being currently developed to remove the hustle of using `google-cloud-aiplatform` with HuggingFace models, providing more extensibility towards HuggingFace's use cases. The interface looks similar to the one defined in `sagemaker`, AWS SageMaker's Python SDK; check it at [`sagemaker.huggingface.HuggingFaceModel`](https://github.com/aws/sagemaker-python-sdk/blob/master/src/sagemaker/huggingface/model.py).
