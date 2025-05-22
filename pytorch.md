# cuda版本

* 3090,A100等只支持CUDA11+
* 4060,H100等只支持CUDA12+，也支持CUDA11+如11.8

## pip/conda 下载各个版本的torchxx

https://anaconda.org/

### nvidia

* https://anaconda.org/nvidia/repo

* cuda-toolkit: [Cuda Toolkit | Anaconda.org](https://anaconda.org/nvidia/cuda-toolkit)

* 添加nvidia package

```bash
conda install pytorch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 pytorch-cuda=12.1 -c pytorch -c nvidia
```

[Previous PyTorch Versions](https://pytorch.org/get-started/previous-versions/)

https://github.com/pytorch/pytorch/wiki/PyTorch-Versions

### nvidia-*-cu11的用法

```bash
nvidia-cublas-cu11        11.11.3.6                pypi_0    pypi
nvidia-cuda-cupti-cu11    11.8.87                  pypi_0    pypi
nvidia-cuda-nvrtc-cu11    11.8.89                  pypi_0    pypi
nvidia-cuda-runtime-cu11  11.8.89                  pypi_0    pypi
nvidia-cudnn-cu11         9.1.0.70                 pypi_0    pypi
nvidia-cufft-cu11         10.9.0.58                pypi_0    pypi
nvidia-curand-cu11        10.3.0.86                pypi_0    pypi
nvidia-cusolver-cu11      11.4.1.48                pypi_0    pypi
nvidia-cusparse-cu11      11.7.5.86                pypi_0    pypi
nvidia-nccl-cu11          2.21.5                   pypi_0    pypi
nvidia-nvtx-cu11          11.8.86                  pypi_0    pypi
```

1. CUDA基础运行时

| 库名                         | 功能                                        |
| -------------------------- | ----------------------------------------- |
| `nvidia-cuda-runtime-cu11` | CUDA 运行时环境（如设备管理、内存操作）的 Python 封装。        |
| `nvidia-cuda-nvrtc-cu11`   | CUDA 运行时编译库（动态编译 CUDA 代码为 PTX 中间表示）。      |
| `nvidia-cuda-cupti-cu11`   | CUDA Profiling Tools Interface（性能分析工具接口）。 |

2. 数学计算库

| 库名                     | 功能                                   |
| ---------------------- | ------------------------------------ |
| `nvidia-cublas-cu11`   | CUDA 基础线性代数库（BLAS），加速矩阵运算（如 `gemm`）。 |
| `nvidia-cufft-cu11`    | CUDA 快速傅里叶变换库（FFT）。                  |
| `nvidia-curand-cu11`   | CUDA 随机数生成库。                         |
| `nvidia-cusolver-cu11` | CUDA 线性代数求解器（如矩阵分解、特征值计算）。           |
| `nvidia-cusparse-cu11` | CUDA 稀疏矩阵运算库。                        |

3. 深度学习相关

| 库名                  | 功能                                        |
| ------------------- | ----------------------------------------- |
| `nvidia-cudnn-cu11` | CUDA 深度神经网络库（cuDNN），提供卷积、池化等操作的优化实现。      |
| `nvidia-nccl-cu11`  | NVIDIA 集合通信库（多卡训练时用于高效通信，如 `all_reduce`）。 |
| `nvidia-nvtx-cu11`  | NVIDIA 工具扩展库（用于标记代码段以方便性能分析）。             |

* isgym中nvidia-*-cu和pytorch的cuda版本一致

### cudatoolkit和nvidia-*-cu11的区别

| **组件类型**            | **功能定位**                                                        | **典型安装方式**                      |
| ------------------- | --------------------------------------------------------------- | ------------------------------- |
| **`nvidia-*-cu11`** | NVIDIA 官方 CUDA 加速库的 **Python 封装版**，通过 PyPI 分发，仅包含必要运行时组件。       | `pip install nvidia-cudnn-cu11` |
| **`cudatoolkit`**   | 完整的 **CUDA 开发工具包**（含编译器 `nvcc`、标准库和工具链），通过 Conda 或 NVIDIA 官网分发。 |                                 |

## conda install如何指定下面的build版本?

```bash
:~$ conda search pytorch
Loading channels: done
# Name                       Version           Build  Channel             
pytorch                       0.1.12          py27_0  anaconda/pkgs/free  
pytorch                       0.1.12    py27_nomkl_0  anaconda/pkgs/free  
pytorch                       0.1.12 py27cuda7.5cudnn5.1_1  anaconda/pkgs/free  
pytorch                       0.1.12 py27cuda7.5cudnn6.0_1  anaconda/pkgs/free  
pytorch                       0.1.12 py27cuda8.0cudnn5.1_1  anaconda/pkgs/free  
pytorch                       0.1.12 py27cuda8.0cudnn6.0_1  anaconda/pkgs/free  
pytorch                       0.1.12          py35_0  anaconda/pkgs/free  
pytorch                       0.1.12    py35_nomkl_0  anaconda/pkgs/free  
pytorch                       0.1.12 py35cuda7.5cudnn5.1_1  anaconda/pkgs/free  
pytorch                       0.1.12 py35cuda7.5cudnn6.0_1  anaconda/pkgs/free
```

* 会默认根据toolkit安装

```bash
conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3
```

* 或者手动指定

```bash
conda install <package-name>=<version>=<build>
conda search pytorch
conda install pytorch=2.5.1=py3.12_cuda12.4_cudnn9.1.0_0
```

# batch training

# cuda out of memory

0. 按批load to gpu
   
   ```py
   for batch_idx, batch_data in enumerate(Test_Loader):
    batch_data = batch_data.to(device)
   ```

对比实验
2. 仅仅将batch_data存储，正常
3. 将神经网络经过模型预测后，无论是否释放模型的输出，都会报错cuda out of memory

* 模型forward的时候保存了计算图,并未清除，可能是这个原因
  
  ```py
    gcnet.eval()
    with torch.no_grad():
        pos, _, _, _ = gcnet(batch_data)
  ```
3. 训练的时候
* first define a optimizer
  
  ```py
  optimizer = torch.optim.SGD(model.parameters(), lr=learning_rate)
  ```

* 参数梯度清零
  
  ```py
    optimizer.zero_grad()
  ```

* 参数迭代不计算梯度
  
  ```py
    optimizer.step()
  ```

* [some little stupid but rich functions](https://stackoverflow.com/questions/59129812/how-to-avoid-cuda-out-of-memory-in-pytorch)
