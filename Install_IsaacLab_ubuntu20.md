# 安装(已解决)

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
...
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
  ...
  Installing collected packages: isaaclab_mimic
  Attempting uninstall: isaaclab_mimic
    Found existing installation: isaaclab_mimic 1.0.3
    Uninstalling isaaclab_mimic-1.0.3:
      Successfully uninstalled isaaclab_mimic-1.0.3
  Successfully installed isaaclab_mimic-1.0.3
  [INFO] Running inside a docker container. Skipping VSCode settings setup.
  [INFO] To setup VSCode settings, run 'isaaclab -v'.
  ```
  
  # 执行教程用例
  
  ```bash
  python scripts/tutorials/00_sim/create_empty.py  --headless
  ```
  
  ## waring 1
  
  > 2025-04-08 06:54:50 [0ms] [Warning] [omni.kit.app.plugin] No crash reporter present, dumps uploading isn't available.
  > 2025-04-08 06:54:50 [538ms] [Warning] [omni.usd_config.extension] Enable omni.materialx.libs extension to use MaterialX
  > 2025-04-08 06:54:50 [646ms] [Warning] [omni.platforminfo.plugin] failed to open the default display.  Can't verify X Server version.
  > 2025-04-08 06:54:51 [843ms] [Warning] [omni.datastore] OmniHub is inaccessible
  > 2025-04-08 06:54:51 [1,038ms] [Warning] [omni.isaac.dynamic_control] omni.isaac.dynamic_control is deprecated as of Isaac Sim 4.5. No action is needed from end-users.

* 然后一直卡着不动
  
  ```bash
  |---------------------------------------------------------------------------------------------|
  | Driver Version: 535.183.06    | Graphics API: Vulkan
  |=============================================================================================|
  | GPU | Name                             | Active | LDA | GPU Memory | Vendor-ID | LUID       |
  |     |                                  |        |     |            | Device-ID | UUID       |
  |     |                                  |        |     |            | Bus-ID    |            |
  |---------------------------------------------------------------------------------------------|
  | 0   | NVIDIA GeForce RTX 3090          | Yes: 0 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | a9161167.. |
  |     |                                  |        |     |            | 1         |            |
  |---------------------------------------------------------------------------------------------|
  | 1   | NVIDIA GeForce RTX 3090          | Yes: 1 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | 3e9126d4.. |
  |     |                                  |        |     |            | 25        |            |
  |---------------------------------------------------------------------------------------------|
  | 2   | NVIDIA GeForce RTX 3090          | Yes: 2 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | 395c07c8.. |
  |     |                                  |        |     |            | 41        |            |
  |---------------------------------------------------------------------------------------------|
  | 3   | NVIDIA GeForce RTX 3090          | Yes: 3 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | 26522d15.. |
  |     |                                  |        |     |            | 61        |            |
  |---------------------------------------------------------------------------------------------|
  | 4   | NVIDIA GeForce RTX 3090          | Yes: 4 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | 7481c43c.. |
  |     |                                  |        |     |            | 81        |            |
  |---------------------------------------------------------------------------------------------|
  | 5   | NVIDIA GeForce RTX 3090          | Yes: 5 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | d3dde8e2.. |
  |     |                                  |        |     |            | a1        |            |
  |---------------------------------------------------------------------------------------------|
  | 6   | NVIDIA GeForce RTX 3090          | Yes: 6 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | d3dddf8d.. |
  |     |                                  |        |     |            | c1        |            |
  |---------------------------------------------------------------------------------------------|
  | 7   | NVIDIA GeForce RTX 3090          | Yes: 7 |     | 24822   MB | 10de      | 0          |
  |     |                                  |        |     |            | 2204      | e303f251.. |
  |     |                                  |        |     |            | e1        |            |
  |=============================================================================================|
  | OS: 20.04.1 LTS (Focal Fossa) ubuntu, Version: 20.04.1, Kernel: 5.4.0-190-generic
  | Processor: AMD EPYC 7702 64-Core Processor
  | Cores: 128 | Logical Cores: 128
  |---------------------------------------------------------------------------------------------|
  | Total Memory (MB): 515809 | Free Memory: 136335
  | Total Page/Swap (MB): 8191 | Free Page/Swap: 8091
  |---------------------------------------------------------------------------------------------|
  [INFO]: Setup complete...
  ```

## 执行rl环境

```bash
./isaaclab.sh -p scripts/reinforcement_learning/rsl_rl/train.py --task=Isaac-Ant-v0 --headless
```

* 由前面的报错，还有

> 2025-04-08 06:56:22 [384,292ms] [Warning] [omni.usd] Warning: in _ReportErrors at line 2890 of /builds/omniverse/usd-ci/USD/pxr/usd/usd/stage.cpp -- In </World/envs/env_0/Robot>: Could not open asset @http://omniverse-content-production.s3-us-west-2.amazonaws.com/Assets/Isaac/4.5/Isaac/IsaacLab/Robots/Classic/Cartpole/cartpole.usd@ for reference introduced by @anon:0xc7493d0:World0.usd@</World/envs/env_0/Robot>. (recomposing stage on stage @anon:0xc7493d0:World0.usd@ <0xc74e200>)
