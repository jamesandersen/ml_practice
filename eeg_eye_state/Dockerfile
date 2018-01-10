ARG TAG_VERSION=latest

FROM jupyter/minimal-notebook:${TAG_VERSION}

USER root
RUN apt-get update && \
    apt-get install -y --no-install-recommends libav-tools && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip install h5py tensorflow==1.5.0rc0 keras matplotlib seaborn

USER $NB_USER