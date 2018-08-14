FROM pytorch/pytorch:0.4_cuda9_cudnn7
MAINTAINER Louis Tiao <louistiao@me.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
        wget \
        unzip \
        && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix cyclegan && \
    cd cyclegan && \
    pip install --no-cache-dir -r requirements.txt

WORKDIR /workspace/cyclegan

EXPOSE 8097
