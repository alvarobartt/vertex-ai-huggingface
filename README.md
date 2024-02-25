# Vertex AI 🤝🏻 HuggingFace

🤗 Collection of examples on how to train, deploy and monitor HuggingFace models in Google Cloud Vertex AI

## Installation and setup

_A Google Cloud account must exist in advance, and the user should have enough (lets say admin) permissions on Vertex AI, as well as permissions on Cloud Storage and Container Registry; as those are the main services that will be used. Additionally, all the APIs affecting those services and their interconnections should be enabled. Anyway, the permission level is mentioned within each notebook separately when needed._

* `gcloud` CLI needs to be installed and logged in the project that will be used. See the installation notes at https://cloud.google.com/sdk/docs/install

* `docker` needs to be installed locally, and up and running, since it will be used to build the CPR images before pushing those to the container registry. See the installation notes at https://docs.docker.com/engine/install/

* `google-cloud-aiplatform` Python library is required to programatically build the CPR image and to define the custom prediction code via a custom `Predictor`.

    `pip install google-cloud-aiplatform --upgrade`

* `git lfs` needs to be installed for pulling / cloning models from the HuggingFace Hub.

## Contents

* [`online-prediction/`](./online-prediction): contains some notebooks to explain the different steps to upload, register and deploy any model from the HuggingFace Hub in Vertex AI, covering both CPU-only and GPU accelerated inference.

## What's next?

This collection will be updated iteratively, and here are some of the things that are currently under development and will be published soon:

* [ ] `pipelines/`: contains some notebooks to explain how to build custom pipelines, focusing in fine-tuning of HuggingFace models (which could later be deployed within Vertex AI)
* [ ] `batch-predictions/`: contains some notebooks to explain the concept of batch predictions, comparing those to online predictions, and also providing some practical use cases
* [ ] `real-time-inference/sentence-transformers/`: contains some notebooks explaining how to upload, register and deploy `SentenceTransformers` models in Vertex AI

Additionally, a Python package is being currently developed to remove the hustle of using `google-cloud-aiplatform` and to manually define everything, while everything will be done similarly to how it's done in `sagemaker` which is AWS SageMaker's Python SDK, more information about the tentative approach pattern at [`sagemaker.huggingface.HuggingFaceModel`](https://github.com/aws/sagemaker-python-sdk/blob/master/src/sagemaker/huggingface/model.py).