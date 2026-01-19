# Task-based Adaptive Transmit Beamforming for Efficient Ultrasound Quantification

The repo contains the code for the paper _Task-based Adaptive Transmit Beamforming for Efficient Ultrasound Quantification_.

Online transmit-scheme optimization designed to minimize uncertainty about downstream measurement parameters, enabling high quality estimates using a small fraction of the transmit events typically necessary.

![lvid_measurements_timeseries](https://github.com/user-attachments/assets/dc98cb43-99cf-4fa2-94f1-57cfd8d958da)

Find the weights of our models on Huggingface:
- [EchoNetLVH Segmentation Model](https://huggingface.co/zeahub/echonetlvh)
- [EchoNetLVH Diffusion Model](https://huggingface.co/zeahub/diffusion-echonetlvh)

## Setup code

Install [`zea`](https://github.com/tue-bmd/zea), the cognitive ultrasound toolbox.

```bash
pip install "zea==0.0.4"
```

or use the submodule in this repo:

```bash
git submodule update --init --recursive
pip install -e zea
```

Install other dependencies for this repo:

```bash
KERAS_VER=$(python3 -c "import keras; print(keras.__version__)")
pip install tf2jax==0.3.6 pandas jaxwt dm-pix jax
pip install keras==${KERAS_VER}
cp .env.example .env
touch users.yaml # edit!
```

## Dataset

- Download the [EchoNetLVH dataset](https://echonet.github.io/lvh/index.html#dataset).

- Convert the dataset to the polar format using the `zea` conversion scripts described [here](https://github.com/tue-bmd/zea/tree/main/zea/data/convert/echonetlvh).


## Example Notebook
See the `zea` example notebook implementing the task-based perception action loop, [here](https://zea.readthedocs.io/en/latest/notebooks/agent/task_based_perception_action_loop.html).
