# Lightning-Fast Modulation Classification with Hardware-Efficient Neural Networks submission

This repository contains the submission of our team (**Team Velocity**) for the problem statement [Lightning-Fast Modulation Classification with Hardware-Efficient Neural Networks](https://challenge.aiforgood.itu.int/match/matchitem/34) in the **ITU AI/ML in 5G Challenge**.


## Prerequisites

The sandbox was tested on Ubuntu, but the containerized setup should work on most platforms.

- Install Docker Engine
  - Convenient install script: [get.docker.com](https://get.docker.com)
  - Full installation instructions:  [docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)
  - To use docker without `sudo` you should follow these [instructions](https://docs.docker.com/engine/install/linux-postinstall/) to add your user to the `docker group`
- Optional steps to enable GPU-accelerated training (recommended)
  - Install current NVIDIA driver
  - Install NVIDIA Container Toolkit, see instructions here: [github.com/NVIDIA/nvidia-docker](https://github.com/NVIDIA/nvidia-docker)

## Using the sandbox notebook

1. Clone this repository
2. Set optional environment variables
   - `DATASET_DIR`: This directory will be mounted inside the container at "/workspace/dataset", download instructions can be found inside the Jupyter notebook
   - `DOCKER_GPUS`: Select GPUs which will be accessible from within the container, for example `all` or `device=0`
   - `JUPYTER_PORT`: Override default port (8888)
   - `NETRON_PORT`: Override default port (8081)
   - `JUPYTER_PASSWD_HASH`: Override default password ("radioml")
   - `LOCALHOST_URL`: Set the IP/URL of the machine if you don't access it via `localhost`
3. Run `chmod u+x run-docker.sh` inside the `submission/` to create the executable file.
3. Run `./run_docker.sh` inside `submission/` to launch the Jupyter notebook server
   - Alternatively for experimenting: Run `./run_docker.sh bash` to launch an interactive shell
4. Connect to `http://HOSTNAME:JUPYTER_PORT` from a browser and login with password "radioml"
5. Run the code block by block.
