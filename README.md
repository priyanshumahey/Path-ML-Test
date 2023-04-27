# Path-ML-Test

## Setup with PIP (not recommended)

To set up path-ml, we'll need to run the following (for windows):

``` shell
conda create --name pathml python=3.8
conda activate pathml
```

Then we install OpenJDK 8

``` shell
conda install openjdk==8.0.152
```

and finally we install path-ml using

```shell
pip install pathml
```

To set up your GPU, you'll need to do the following:

``` shell
nvidia-smi
```

and then you'll install the correct version of `cudatoolkit`:

``` shell
conda install cudatoolkit=11.0
```

And then verify that your GPU does indeed work:

``` shell
python -c "import torch; print(torch.cuda.is_available())"
```

## Setup with Docker

Download PathML container from Docker Hub:

``` shell
docker pull pathml/pathml:latest
```

Then connect to the container using:

``` shell
docker run -it -p 8888:8888 pathml/pathml
```
