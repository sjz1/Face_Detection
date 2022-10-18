# Face_Detection
Reference : FaceNet : nn2 model

# Setting
#### 1. make virtual environment

```anaconda
conda create -n torch python=3.7
```
(for torch you should install python ver : 3.7)

#### 2. activate your virtual environment
```anaconda
conda activate pytorch 
```
<----->
```anaconda
conda deactivate
```

#### 3. install pytorch

```anaconda
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
```
or if you only want to use cpu 
```anaconda
conda install pytorch torchvision cpuonly -c pytorch
```
#### 4. install another libraries
```anaconda
conda install jupyter pandas matplotlib opencv
```

# Installation
Reference : [FaceNet-Pytorch](https://github.com/timesler/facenet-pytorch)

| Python | 3.7 | 3.6 | 3.5 |
| :---: | :---: | :---: | :---: |
| Status | [![Build Status](https://travis-ci.com/timesler/facenet-pytorch.svg?branch=master)](https://travis-ci.com/timesler/facenet-pytorch) | [![Build Status](https://travis-ci.com/timesler/facenet-pytorch.svg?branch=master)](https://travis-ci.com/timesler/facenet-pytorch) | [![Build Status](https://travis-ci.com/timesler/facenet-pytorch.svg?branch=master)](https://travis-ci.com/timesler/facenet-pytorch) |

    ```bash
    # With pip:
    pip install facenet-pytorch
    
    # or clone this repo, removing the '-' to allow python imports:
    git clone https://github.com/timesler/facenet-pytorch.git facenet_pytorch
    
    # or use a docker container (see https://github.com/timesler/docker-jupyter-dl-gpu):
    docker run -it --rm timesler/jupyter-dl-gpu pip install facenet-pytorch && ipython
    ```

In python, import facenet-pytorch and instantiate models:
    
    ```python
    from facenet_pytorch import MTCNN, InceptionResnetV1
    
    # If required, create a face detection pipeline using MTCNN:
    mtcnn = MTCNN(image_size=<image_size>, margin=<margin>)
    
    # Create an inception resnet (in eval mode):
    resnet = InceptionResnetV1(pretrained='vggface2').eval()
    ```
