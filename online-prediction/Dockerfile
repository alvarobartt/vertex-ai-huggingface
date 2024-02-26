FROM nvidia/cuda:12.3.0-base-ubuntu22.04 AS build
LABEL maintainer="Alvaro Bartolome"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install python3 python3-pip -y

RUN ln -s /usr/bin/python3 /usr/bin/python
ENV PYTHON=/usr/bin/python

ARG TORCH="2.2.0"

RUN python -m pip install --no-cache-dir --upgrade pip && \
    python -m pip install --no-cache-dir torch==${TORCH}