# Assigning GPU to your Python program
## Step 1 Checking out your GPUs firstly via `nvidia-smi`
```bash
$ nvidia-smi
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 470.129.06   Driver Version: 470.129.06   CUDA Version: 11.4     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ...  Off  | 00000000:18:00.0 Off |                  N/A |
| 82%   84C    P2   203W / 250W |   4751MiB / 11019MiB |     74%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   1  NVIDIA GeForce ...  Off  | 00000000:5E:00.0 Off |                  N/A |
| 35%   30C    P8    15W / 250W |      3MiB / 11019MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   2  NVIDIA GeForce ...  Off  | 00000000:AF:00.0 Off |                  N/A |
| 35%   29C    P8     5W / 250W |   1830MiB / 11019MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   3  NVIDIA GeForce ...  Off  | 00000000:D8:00.0 Off |                  N/A |
| 41%   35C    P8    15W / 260W |   1830MiB / 11019MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
+-----------------------------------------------------------------------------+
```
## Step 2  Two methods
Both methods are actually to set the environmental variables, and consequently, the program only can touches `GPU0` and `GPU1` in examples below.
1. Setting environmental variables via terminal.
```bash
$ CUDA_VISIBLE_DEVICES=0,1 python test.py 
```

2. Setting environmental variables inside `.py` file
```python
# test.py
import os
os.environ["CUDA_VISIBLE_DEVICES"] = "0,1"
```




