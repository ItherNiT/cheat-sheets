
Install nvidia docker container toolkit:
```
sudo apt-get update \
    && sudo apt-get install -y nvidia-container-toolkit-base
```

or 

```
sudo apt-get install -y nvidia-container-toolkit
```

apply the changes to docker:

```
sudo nvidia-ctk runtime configure --runtime=docker
```

restart docker:
```
sudo systemctl restart docker
```

test using: 

```
sudo docker run --rm --runtime=nvidia --gpus all nvidia/cuda:11.6.2-base-ubuntu20.04 nvidia-smi
```
