# Setup

Build the image:
`docker build --rm -f Dockerfile -t eeg_eye_state:latest eeg_eye_state`

Checkout the docker image:
`docker run -it eeg_eye_state:latest bash -c "python -c 'import keras; print(keras.__version__)'"`

Startup jupyter:

```bash
    docker run -it -p 8888:8888 \
        -v `pwd`:/home/jovyan/work \
        eeg_eye_state:latest
```