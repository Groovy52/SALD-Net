# Instrallation
The overall code framework was developed with reference to [OpenPCDet](https://github.com/open-mmlab/OpenPCDet/tree/master).  
The environment was built using **Docker**, following the [OpenPCDet Docker setup guide](https://github.com/open-mmlab/OpenPCDet/tree/master/docker), which provides advantages such as **easy deployment**, **scalability**, and **consistency across systems**.

## Build Docker
### 1. With this Docker Imagefile
a. Clone this/OpenPCDet repository

```bash
git clone https://github.com/Groovy52/SALD-Net.git
or
git clone https://github.com/open-mmlab/OpenPCDet.git
```

b. Build docker image that support OpenPCDet through:

```bash
docker build ./ -t saldnet-docker
or
docker build ./ -t openpcdet-docker
```

### 2. With Dockerhub Imagefile
a. Build docker image that support OpenPCDet env (CUDA 11+, Ubuntu 18.04+)
from [Dockerhub](https://hub.docker.com/r/nvidia/cuda)

```
docker pull [image name from Hub]
```

```bash
docker run -it --rm --name [Container name to use] \
--ipc=host --gpus all -p xxxx:xxxx \
--shm-size=[128 or etc..]G \
-v [Host directory path=> ex: /D:~]:[Container path=> ex: /workspace/~] \
[image name from Hub] \
bash
```

### 3. Install `spconv`
```bash
git clone -b v1.2.1 https://github.com/djiajunustc/spconv spconv --recursive
cd spconv
python setup.py bdist_wheel
cd ./dist
pip install *.whl
```

## Requirements
All the codes are tested in the following environment:
-  Linux (tested on Ubuntu 18.04/20.04)
-  Python 3.6+
-  PyTorch 1.1 or higher (tested on PyTorch 1.1, 1,3, 1,5
-  CUDA 11 or higher (tested of CUDA 11.6)
-  spconv 1.2.1 

### 1. Install dependent libraries as follows:
```
cd SALD-Net
pip install -r requirements.txt
python ./setup.py develop
```

### ref this error 
Please refer to the following link for solutions to errors that may occur during the above process.
