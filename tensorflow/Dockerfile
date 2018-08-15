FROM tensorflow/tensorflow:1.10.0-gpu-py3
MAINTAINER Louis Tiao <louistiao@me.com>

ENV LC_ALL C.UTF-8
ENV LANG C.UTF-8

RUN echo ttf-mscorefonts-installer msttcorefonts/accepted-mscorefonts-eula select true | debconf-set-selections
RUN apt-get update && apt-get install -y --no-install-recommends \
        texlive-full \
        msttcorefonts \
        graphviz \
        && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* ~/.cache/matplotlib

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app