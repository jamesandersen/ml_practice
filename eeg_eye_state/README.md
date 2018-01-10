# Setup

1. Build the image initially (or after changing the `Dockerfile`):

```bash
# Creates a local eeg_eye_state:latest image
docker build --rm -f Dockerfile -t eeg_eye_state:latest .
```

2. Checkout the docker image:

```bash
# test that keras can be imported (which in turns tests Tensorflow installation)
docker run -it eeg_eye_state:latest bash -c "python -c 'import keras; print(keras.__version__)'"
```

3. Startup jupyter:

```bash
# Launch a container running a Jupyter notebook
docker run -it -p 8888:8888 \
    -v `pwd`:/home/jovyan \
    eeg_eye_state:latest
```