
# 安装
when I implement the following command according to [Official Install COurses](https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/binaries_installation.html)
```python
./isaaclab.sh --install # or "./isaaclab.sh -i"
```
## 报错
```bash
...
Successfully built isaaclab
Installing collected packages: isaaclab
  Attempting uninstall: isaaclab
    Found existing installation: isaaclab 0.36.5
    Uninstalling isaaclab-0.36.5:
      Successfully uninstalled isaaclab-0.36.5
Successfully installed isaaclab-0.36.5
...
Successfully built isaaclab_assets
Installing collected packages: isaaclab_assets
  Attempting uninstall: isaaclab_assets
    Found existing installation: isaaclab_assets 0.2.1
    Uninstalling isaaclab_assets-0.2.1:
      Successfully uninstalled isaaclab_assets-0.2.1
Successfully installed isaaclab_assets-0.2.1
...
Successfully built isaaclab_mimic
Installing collected packages: isaaclab_mimic
  Attempting uninstall: isaaclab_mimic
    Found existing installation: isaaclab_mimic 1.0.3
    Uninstalling isaaclab_mimic-1.0.3:
      Successfully uninstalled isaaclab_mimic-1.0.3
Successfully installed isaaclab_mimic-1.0.3
...
Successfully built isaaclab_rl
Installing collected packages: isaaclab_rl
  Attempting uninstall: isaaclab_rl
    Found existing installation: isaaclab_rl 0.1.3
    Uninstalling isaaclab_rl-0.1.3:
      Successfully uninstalled isaaclab_rl-0.1.3
Successfully installed isaaclab_rl-0.1.3
...
Successfully built isaaclab_tasks
Installing collected packages: isaaclab_tasks
  Attempting uninstall: isaaclab_tasks
    Found existing installation: isaaclab_tasks 0.10.27
    Uninstalling isaaclab_tasks-0.10.27:
      Successfully uninstalled isaaclab_tasks-0.10.27
Successfully installed isaaclab_tasks-0.10.27

[INFO] Installing extra requirements such as learning frameworks...
[INFO] Installing all rl-frameworks...

Obtaining file:///home/chenlei/IsaacLab/source/isaaclab_rl
  Installing build dependencies ... done
  Checking if build backend supports build_editable ... done
  Getting requirements to build editable ... done
  Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: numpy in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from isaaclab_rl==0.1.3) (1.26.0)
Requirement already satisfied: torch==2.5.1 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from isaaclab_rl==0.1.3) (2.5.1+cu118)
Requirement already satisfied: torchvision>=0.14.1 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from isaaclab_rl==0.1.3) (0.20.1+cu118)
Requirement already satisfied: protobuf<5.0.0,>=3.20.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (3.20.3)
Requirement already satisfied: hydra-core in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (1.3.2)
Requirement already satisfied: h5py in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (3.13.0)
Requirement already satisfied: tensorboard in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (2.19.0)
Requirement already satisfied: moviepy in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (1.0.3)
Requirement already satisfied: pillow==11.0.0 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from isaaclab_rl==0.1.3) (11.0.0)
Requirement already satisfied: filelock in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (3.15.4)
Requirement already satisfied: typing-extensions>=4.8.0 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (4.11.0)
Requirement already satisfied: networkx in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (3.4.2)
Requirement already satisfied: jinja2 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (3.1.4)
Requirement already satisfied: fsspec in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (2024.10.0)
Requirement already satisfied: nvidia-cuda-nvrtc-cu11==11.8.89 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.8.89)
Requirement already satisfied: nvidia-cuda-runtime-cu11==11.8.89 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.8.89)
Requirement already satisfied: nvidia-cuda-cupti-cu11==11.8.87 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.8.87)
Requirement already satisfied: nvidia-cudnn-cu11==9.1.0.70 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (9.1.0.70)
Requirement already satisfied: nvidia-cublas-cu11==11.11.3.6 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.11.3.6)
Requirement already satisfied: nvidia-cufft-cu11==10.9.0.58 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (10.9.0.58)
Requirement already satisfied: nvidia-curand-cu11==10.3.0.86 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (10.3.0.86)
Requirement already satisfied: nvidia-cusolver-cu11==11.4.1.48 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.4.1.48)
Requirement already satisfied: nvidia-cusparse-cu11==11.7.5.86 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.7.5.86)
Requirement already satisfied: nvidia-nccl-cu11==2.21.5 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (2.21.5)
Requirement already satisfied: nvidia-nvtx-cu11==11.8.86 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (11.8.86)
Requirement already satisfied: triton==3.1.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from torch==2.5.1->isaaclab_rl==0.1.3) (3.1.0)
Requirement already satisfied: sympy==1.13.1 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from torch==2.5.1->isaaclab_rl==0.1.3) (1.13.1)
Requirement already satisfied: mpmath<1.4,>=1.1.0 in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from sympy==1.13.1->torch==2.5.1->isaaclab_rl==0.1.3) (1.3.0)
Requirement already satisfied: stable-baselines3>=2.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (2.6.0)
Requirement already satisfied: rsl-rl-lib==2.3.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (2.3.0)
Requirement already satisfied: gym in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (0.23.1)
Requirement already satisfied: rl-games==1.6.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (1.6.1)
Requirement already satisfied: skrl>=1.4.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_rl==0.1.3) (1.4.3)
Requirement already satisfied: PyYAML<7.0,>=6.0 in /home/chenlei/isaacsim/exts/omni.pip.compute/pip_prebundle (from rl-games==1.6.1->isaaclab_rl==0.1.3) (6.0.1)
Requirement already satisfied: opencv-python<5.0.0,>=4.5.5 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rl-games==1.6.1->isaaclab_rl==0.1.3) (4.11.0.86)
Requirement already satisfied: psutil<6.0.0,>=5.9.0 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from rl-games==1.6.1->isaaclab_rl==0.1.3) (5.9.8)
Requirement already satisfied: setproctitle<2.0.0,>=1.2.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rl-games==1.6.1->isaaclab_rl==0.1.3) (1.3.5)
Requirement already satisfied: tensorboardX<3.0,>=2.5 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rl-games==1.6.1->isaaclab_rl==0.1.3) (2.6.2.2)
Requirement already satisfied: wandb<0.13.0,>=0.12.11 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rl-games==1.6.1->isaaclab_rl==0.1.3) (0.12.21)
Requirement already satisfied: GitPython in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rsl-rl-lib==2.3.0->isaaclab_rl==0.1.3) (3.1.44)
Requirement already satisfied: onnx in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from rsl-rl-lib==2.3.0->isaaclab_rl==0.1.3) (1.16.1)
Requirement already satisfied: cloudpickle>=1.2.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from gym->isaaclab_rl==0.1.3) (3.1.1)
Requirement already satisfied: gym_notices>=0.0.4 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from gym->isaaclab_rl==0.1.3) (0.0.8)
Requirement already satisfied: gymnasium in /home/chenlei/isaacsim/exts/omni.isaac.ml_archive/pip_prebundle (from skrl>=1.4.2->isaaclab_rl==0.1.3) (0.29.1)
Requirement already satisfied: packaging in /home/chenlei/isaacsim/exts/omni.isaac.core_archive/pip_prebundle (from skrl>=1.4.2->isaaclab_rl==0.1.3) (23.0)
Requirement already satisfied: tqdm in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from skrl>=1.4.2->isaaclab_rl==0.1.3) (4.67.1)
Requirement already satisfied: pandas in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from stable-baselines3>=2.1->isaaclab_rl==0.1.3) (2.2.3)
Requirement already satisfied: matplotlib in /home/chenlei/isaacsim/exts/omni.isaac.core_archive/pip_prebundle (from stable-baselines3>=2.1->isaaclab_rl==0.1.3) (3.8.4)
Requirement already satisfied: absl-py>=0.4 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (2.2.2)
Requirement already satisfied: grpcio>=1.48.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (1.71.0)
Requirement already satisfied: markdown>=2.6.8 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (3.7)
Requirement already satisfied: setuptools>=41.0.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (75.8.0)
Requirement already satisfied: six>1.9 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from tensorboard->isaaclab_rl==0.1.3) (1.16.0)
Requirement already satisfied: tensorboard-data-server<0.8.0,>=0.7.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (0.7.2)
Requirement already satisfied: werkzeug>=1.0.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from tensorboard->isaaclab_rl==0.1.3) (3.1.3)
Requirement already satisfied: omegaconf<2.4,>=2.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from hydra-core->isaaclab_rl==0.1.3) (2.3.0)
Requirement already satisfied: antlr4-python3-runtime==4.9.* in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from hydra-core->isaaclab_rl==0.1.3) (4.9.3)
Requirement already satisfied: decorator<5.0,>=4.0.2 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from moviepy->isaaclab_rl==0.1.3) (4.4.2)
Requirement already satisfied: imageio<3.0,>=2.5 in /home/chenlei/isaacsim/exts/omni.pip.compute/pip_prebundle (from moviepy->isaaclab_rl==0.1.3) (2.22.2)
Requirement already satisfied: imageio_ffmpeg>=0.2.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from moviepy->isaaclab_rl==0.1.3) (0.6.0)
Requirement already satisfied: requests<3.0,>=2.8.1 in /home/chenlei/isaacsim/exts/omni.pip.cloud/pip_prebundle (from moviepy->isaaclab_rl==0.1.3) (2.32.3)
Requirement already satisfied: proglog<=1.0.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from moviepy->isaaclab_rl==0.1.3) (0.1.11)
Requirement already satisfied: pygame==2.1.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from gym[classic-control]<0.24.0,>=0.23.0->rl-games==1.6.1->isaaclab_rl==0.1.3) (2.1.0)
Requirement already satisfied: farama-notifications>=0.0.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from gymnasium->skrl>=1.4.2->isaaclab_rl==0.1.3) (0.0.4)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from requests<3.0,>=2.8.1->moviepy->isaaclab_rl==0.1.3) (3.3.2)
Requirement already satisfied: idna<4,>=2.5 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from requests<3.0,>=2.8.1->moviepy->isaaclab_rl==0.1.3) (3.6)
Requirement already satisfied: urllib3<3,>=1.21.1 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from requests<3.0,>=2.8.1->moviepy->isaaclab_rl==0.1.3) (2.2.3)
Requirement already satisfied: certifi>=2017.4.17 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from requests<3.0,>=2.8.1->moviepy->isaaclab_rl==0.1.3) (2024.8.30)
Requirement already satisfied: Click!=8.0.0,>=7.0 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (8.1.7)
Requirement already satisfied: promise<3,>=2.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (2.3)
Requirement already satisfied: shortuuid>=0.5.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (1.0.13)
Requirement already satisfied: sentry-sdk>=1.0.0 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (1.43.0)
Requirement already satisfied: docker-pycreds>=0.4.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (0.4.0)
Requirement already satisfied: pathtools in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from wandb<0.13.0,>=0.12.11->rl-games==1.6.1->isaaclab_rl==0.1.3) (0.1.2)
Requirement already satisfied: gitdb<5,>=4.0.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from GitPython->rsl-rl-lib==2.3.0->isaaclab_rl==0.1.3) (4.0.12)
Requirement already satisfied: MarkupSafe>=2.1.1 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from werkzeug>=1.0.1->tensorboard->isaaclab_rl==0.1.3) (3.0.2)
Requirement already satisfied: contourpy>=1.0.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (1.3.1)
Requirement already satisfied: cycler>=0.10 in /home/chenlei/isaacsim/exts/omni.isaac.core_archive/pip_prebundle (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (0.11.0)
Requirement already satisfied: fonttools>=4.22.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (4.57.0)
Requirement already satisfied: kiwisolver>=1.3.1 in /home/chenlei/isaacsim/exts/omni.isaac.core_archive/pip_prebundle (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (1.4.4)
Requirement already satisfied: pyparsing>=2.3.1 in /home/chenlei/isaacsim/exts/omni.isaac.core_archive/pip_prebundle (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (3.0.9)
Requirement already satisfied: python-dateutil>=2.7 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from matplotlib->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (2.9.0.post0)
Requirement already satisfied: pytz>=2020.1 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from pandas->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (2024.1)
Requirement already satisfied: tzdata>=2022.7 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from pandas->stable-baselines3>=2.1->isaaclab_rl==0.1.3) (2025.2)
Requirement already satisfied: smmap<6,>=3.0.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from gitdb<5,>=4.0.1->GitPython->rsl-rl-lib==2.3.0->isaaclab_rl==0.1.3) (5.0.2)
Building wheels for collected packages: isaaclab_rl
  Building editable for isaaclab_rl (pyproject.toml) ... done
  Created wheel for isaaclab_rl: filename=isaaclab_rl-0.1.3-0.editable-py3-none-any.whl size=3452 sha256=65ccba6e1a0481479f8eb488499c4f5c636da9021dd1c6e2b37928b2e9bda61e
  Stored in directory: /tmp/pip-ephem-wheel-cache-smd9ycre/wheels/ab/fa/4d/3337d1e91ecd81d09af73c0d727dff5f467a28400d3bf6480a
Successfully built isaaclab_rl
Installing collected packages: isaaclab_rl
  Attempting uninstall: isaaclab_rl
    Found existing installation: isaaclab_rl 0.1.3
    Uninstalling isaaclab_rl-0.1.3:
      Successfully uninstalled isaaclab_rl-0.1.3
Successfully installed isaaclab_rl-0.1.3
Looking in indexes: https://mirrors.aliyun.com/pypi/simple/
Obtaining file:///home/chenlei/IsaacLab/source/isaaclab_mimic
  Installing build dependencies ... done
  Checking if build backend supports build_editable ... done
  Getting requirements to build editable ... done
  Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: tomli in /home/chenlei/isaacsim/exts/isaacsim.asset.exporter.urdf/pip_prebundle (from isaaclab_mimic==1.0.3) (2.0.1)
Requirement already satisfied: ipywidgets==8.1.5 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_mimic==1.0.3) (8.1.5)
Requirement already satisfied: comm>=0.1.3 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.2.2)
Requirement already satisfied: ipython>=6.1.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (8.35.0)
Requirement already satisfied: traitlets>=4.3.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (5.14.3)
Requirement already satisfied: widgetsnbextension~=4.0.12 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (4.0.13)
Requirement already satisfied: jupyterlab-widgets~=3.0.12 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (3.0.13)
Collecting robomimic@ git+https://github.com/ARISE-Initiative/robomimic.git (from isaaclab_mimic==1.0.3)
  Cloning https://github.com/ARISE-Initiative/robomimic.git to /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff
  Running command git clone --filter=blob:none --quiet https://github.com/ARISE-Initiative/robomimic.git /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff
  error: RPC failed; HTTP 408 curl 22 The requested URL returned error: 408
  fatal: the remote end hung up unexpectedly
  warning: Clone succeeded, but checkout failed.
  You can inspect what was checked out with 'git status'
  and retry with 'git restore --source=HEAD :/'

  error: subprocess-exited-with-error
  
  × git clone --filter=blob:none --quiet https://github.com/ARISE-Initiative/robomimic.git /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff did not run successfully.
  │ exit code: 128
  ╰─> See above for output.
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× git clone --filter=blob:none --quiet https://github.com/ARISE-Initiative/robomimic.git /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff did not run successfully.
│ exit code: 128
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
```
* 于是进入isaaclab_mimic目录,编译执行
```
cd ~/IsaacLab/source/isaaclab_mimic
pip install -e .
```
* 执行正常
* 报错是git clone的问题,根据连接[111](https://stackoverflow.com/questions/22369200/git-pull-push-error-rpc-failed-result-22-http-code-408)
```python
git config http.postBuffer 524288000
git config http.lowSpeedTime 600
```
还是报错
```bash
(mylab) chenlei@118:~/IsaacLab/robomimic$ git clone --filter=blob:none --quiet https://github.com/ARISE-Initiative/robomimic.git /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff
error: RPC failed; HTTP 408 curl 22 The requested URL returned error: 408
fatal: the remote end hung up unexpectedly
warning: Clone succeeded, but checkout failed.
You can inspect what was checked out with 'git status'
and retry with 'git restore --source=HEAD :/'
```
* 但直接执行如下命令有效
```bash
git clone --quiet https://github.com/ARISE-Initiative/robomimic.git /tmp/pip-install-fzzo6zoi/robomimic_cc0f495668f24e26ad9e4c1dfea921ff
```
* 在服务器上无法activate expressvpn

* 阅读setup.py，找到
```py
            ${python_exe} -m pip install -e ${ISAACLAB_PATH}/source/isaaclab_rl["${framework_name}"]  # 302
            ${python_exe} -m pip install -e ${ISAACLAB_PATH}/source/isaaclab_mimic["${framework_name}"]   # 303
```
* 这部分代码安装从source/isaaclab_mimic目录下编译安装源码
* 在isaaclab_mimic/seetup.py中，找到下载robomimic的实现
```py
robomimic@git+https://github.com/ARISE-Initiative/robomimic.git
```
* 不知道怎么消除git clone的静默过滤安装选项，
```py
git clone --filter=blob:none --quiet
```
* 突然想到在外面编译安装robomimic，然后把这个extra package注释在真实安装跳过即可;
## 解决
```bash
Obtaining file:///home/chenlei/IsaacLab/source/isaaclab_mimic
  Installing build dependencies ... done
  Checking if build backend supports build_editable ... done
  Getting requirements to build editable ... done
  Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: tomli in /home/chenlei/isaacsim/exts/isaacsim.asset.exporter.urdf/pip_prebundle (from isaaclab_mimic==1.0.3) (2.0.1)
Requirement already satisfied: ipywidgets==8.1.5 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from isaaclab_mimic==1.0.3) (8.1.5)
Requirement already satisfied: comm>=0.1.3 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.2.2)
Requirement already satisfied: ipython>=6.1.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (8.35.0)
Requirement already satisfied: traitlets>=4.3.1 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (5.14.3)
Requirement already satisfied: widgetsnbextension~=4.0.12 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (4.0.13)
Requirement already satisfied: jupyterlab-widgets~=3.0.12 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (3.0.13)
Requirement already satisfied: decorator in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (4.4.2)
Requirement already satisfied: exceptiongroup in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (1.2.2)
Requirement already satisfied: jedi>=0.16 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.19.2)
Requirement already satisfied: matplotlib-inline in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.1.7)
Requirement already satisfied: pexpect>4.3 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (4.9.0)
Requirement already satisfied: prompt_toolkit<3.1.0,>=3.0.41 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (3.0.50)
Requirement already satisfied: pygments>=2.4.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (2.19.1)
Requirement already satisfied: stack_data in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.6.3)
Requirement already satisfied: typing_extensions>=4.6 in /home/chenlei/isaacsim/extscache/omni.kit.pip_archive-0.0.0+d02c707b.lx64.cp310/pip_prebundle (from ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (4.11.0)
Requirement already satisfied: parso<0.9.0,>=0.8.4 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from jedi>=0.16->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.8.4)
Requirement already satisfied: ptyprocess>=0.5 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from pexpect>4.3->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.7.0)
Requirement already satisfied: wcwidth in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from prompt_toolkit<3.1.0,>=3.0.41->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.2.13)
Requirement already satisfied: executing>=1.2.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from stack_data->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (2.2.0)
Requirement already satisfied: asttokens>=2.1.0 in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from stack_data->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (3.0.0)
Requirement already satisfied: pure-eval in /home/chenlei/miniconda3/envs/mylab/lib/python3.10/site-packages (from stack_data->ipython>=6.1.0->ipywidgets==8.1.5->isaaclab_mimic==1.0.3) (0.2.3)
Building wheels for collected packages: isaaclab_mimic
  Building editable for isaaclab_mimic (pyproject.toml) ... done
  Created wheel for isaaclab_mimic: filename=isaaclab_mimic-1.0.3-0.editable-py3-none-any.whl size=3048 sha256=db22a85f4cf4abec032171fd61ee5e1b4959e9e78468ff10cc3c88d2352ee692
  Stored in directory: /tmp/pip-ephem-wheel-cache-_7wcxbec/wheels/45/16/4c/4f2087802bb0164c09bb88d5ee75ea2bba1394757e36dc027c
Successfully built isaaclab_mimic
Installing collected packages: isaaclab_mimic
  Attempting uninstall: isaaclab_mimic
    Found existing installation: isaaclab_mimic 1.0.3
    Uninstalling isaaclab_mimic-1.0.3:
      Successfully uninstalled isaaclab_mimic-1.0.3
Successfully installed isaaclab_mimic-1.0.3
[INFO] Running inside a docker container. Skipping VSCode settings setup.
[INFO] To setup VSCode settings, run 'isaaclab -v'.
```
# 执行

### 报错1
> 2025-04-08 06:54:50 [0ms] [Warning] [omni.kit.app.plugin] No crash reporter present, dumps uploading isn't available.
> 2025-04-08 06:54:50 [538ms] [Warning] [omni.usd_config.extension] Enable omni.materialx.libs extension to use MaterialX
> 2025-04-08 06:54:50 [646ms] [Warning] [omni.platforminfo.plugin] failed to open the default display.  Can't verify X Server version.
> 2025-04-08 06:54:51 [843ms] [Warning] [omni.datastore] OmniHub is inaccessible
> 2025-04-08 06:54:51 [1,038ms] [Warning] [omni.isaac.dynamic_control] omni.isaac.dynamic_control is deprecated as of Isaac Sim 4.5. No action is needed from end-users.



## 报错2
> 2025-04-08 06:56:22 [384,292ms] [Warning] [omni.usd] Warning: in _ReportErrors at line 2890 of /builds/omniverse/usd-ci/USD/pxr/usd/usd/stage.cpp -- In </World/envs/env_0/Robot>: Could not open asset @http://omniverse-content-production.s3-us-west-2.amazonaws.com/Assets/Isaac/4.5/Isaac/IsaacLab/Robots/Classic/Cartpole/cartpole.usd@ for reference introduced by @anon:0xc7493d0:World0.usd@</World/envs/env_0/Robot>. (recomposing stage on stage @anon:0xc7493d0:World0.usd@ <0xc74e200>)


