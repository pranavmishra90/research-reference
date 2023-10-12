# Preparing your linux computer for next-generation -omics experiments
Pranav Kumar Mishra
Thursday, October 12, 2023

## Overview

- Dotfiles, SSH Keys
- Mambaforge
- Datalad
- R and R Studio
- Nvidia Drivers
- Nvidia CUDA
- Pytorch, Tensorflow, Docker with GPU Passthrough
- Cell Ranger
- Illumina bcl2fastq2

## CUDA

Official instructions from [Nvidia on installing
CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#).
Followed instructions for Ubuntu 22.04 LTS.

### Pytorch, Tensorflow, Docker with GPU Passthrough

Followed and modified instructions from the website by Alex
Watson<sup>1</sup>.

``` {bash}
# Verify that Nvidia drivers are correctly installed
nvidia-smi
```

``` {bash}
# Install PyTorch

#conda create –name=pytorch python=3.9
# I installed these packages into base, since I will be using pytorch wrapped functions
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia

# Verify install
python3 -c "import torch; print(torch.cuda.is_available())"
```

``` {bash}
# Install TensorFlow

conda create --name=tf python=3.9
conda activate tf
conda install -c conda-forge cudatoolkit=11.2.2 cudnn=8.1.0

mkdir -p $CONDA_PREFIX/etc/conda/activate.d
echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/' > $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh

conda activate tf
conda install -c conda-forge tensorflow
```

``` {bash}
# Install GPU support inside docker

distribution=$(. /etc/os-release;echo $ID$VERSION_ID) \
    && curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
  && curl -s -L https://nvidia.github.io/libnvidia-container/$distribution/libnvidia-container.list | \
  sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
  sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
  
sudo apt-get update
sudo apt-get install -y nvidia-container-toolkit
sudo nvidia-ctk runtime configure --runtime=docker
sudo systemctl restart docker

docker run --rm --runtime=nvidia --gpus all nvidia/cuda:11.6.2-base-ubuntu20.04 
nvidia-smi
```

<div id="refs" class="references csl-bib-body">

<div id="ref-alexwatson2023" class="csl-entry">

<span class="csl-left-margin">1.
</span><span class="csl-right-inline">Alex Watson. Install TensorFlow
and PyTorch with CUDA, cUDNN, and GPU Support in 3 Easy Steps. Published
online March 6, 2023.
<https://gretel.ai/blog/install-tensorflow-with-cuda-cdnn-and-gpu-support-in-4-easy-steps></span>

</div>

</div>
