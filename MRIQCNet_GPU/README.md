# DOC for Nvidia GPU machines with CUDA

If you do not want to use Docker, go [here](https://github.com/garciaml/MRIQCNet/tree/master/MRIQCNet_GPU/MRIQCNet_GPU_no_docker) !

## Pre-requisites: 
Nvidia drivers and CUDA installed.

## Step 1: Install Docker

https://docs.docker.com/get-docker/

## Step 2: Install Nvidia Container toolkit

Linux system: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html 

Windows system: use WSL 2 : https://developer.nvidia.com/cuda/wsl
https://docs.nvidia.com/cuda/wsl-user-guide/index.html#known-limitations-for-linux-cuda-apps
Limitations: With the NVIDIA Container Toolkit for Docker 19.03, only --gpus all is supported. On multi-GPU systems it is not possible to filter for specific GPU devices by using specific index numbers to enumerate GPUs. 

## Step 3: Get our docker image

docker pull ...

## Step 4: Run MRIQCNet

1/ Participant-level

2/ Group-level
