# MuJoCo Training on Generative Adversarial Imitation Learning (GAIL) 



## Create Environment on Ubuntu 18.04
Install MuJoCo 1.59
```
mkdir -p /root/.mujoco \
    && wget https://www.roboti.us/download/mjpro150_linux.zip -O mujoco.zip \
    && unzip mujoco.zip -d /root/.mujoco \
    && rm mujoco.zip
COPY ./mjkey.txt /root/.mujoco/
ENV LD_LIBRARY_PATH /root/.mujoco/mjpro150/bin:${LD_LIBRARY_PATH}
```


To fix ```fatal error: GL/osmesa.h: No such file or directory``` install:

```
sudo apt-get install libosmesa6-dev
```

Create Conda Environment with Python 3.5
```
conda env create -f environment.yml
source activate gail-mujoco
```


## Download Expert Data
create a data directory and download the expert from [download link](https://drive.google.com/drive/folders/1h3H4AY_ZBx08hz-Ct0Nxxus-V1melu1U?usp=sharing)

## Run GAIL training on Hopper
```
python -m baselines.gail.run_mujoco
```




## GAIL Training Logs from Yuan-Hong Liao
[https://drive.google.com/drive/folders/1nnU8dqAV9i37-_5_vWIspyFUJFQLCsDD]





