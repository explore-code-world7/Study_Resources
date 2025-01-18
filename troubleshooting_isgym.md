# isgym related

## subprocess.CalledProcessError: Command '['which', 'c++']' returned non-zero exit status 1

lib/python3.8/site-packages/torch/utils/cpp_extension.py", line 311, in check_compiler_ok_for_platform
    which = subprocess.check_output(['which', compiler], stderr=subprocess.STDOUT)
  File "/home/planet/miniconda3/envs/isgym/lib/python3.8/subprocess.py", line 415, in check_output
    return run(*popenargs, stdout=PIPE, timeout=timeout, check=True,
  File "/home/planet/miniconda3/envs/isgym/lib/python3.8/subprocess.py", line 516, in run
    raise CalledProcessError(retcode, process.args,
subprocess.CalledProcessError: Command '['which', 'c++']' returned non-zero exit status 1.

### solution
```cpp
sudo apt install build-essentials
```


##  lib/libstdc++.so.6: version `GLIBCXX_3.4.32' not found
ImportError: /home/user_name/miniconda3/envs/env_name/lib/libstdc++.so.6: version `GLIBCXX_3.4.32' not found (required by /home/planet/.cache/torch_extensions/py38_cu121/gymtorch/gymtorch.so)

### solution
[link](https://stackoverflow.com/questions/76974555/glibcxx-3-4-32-not-found-error-at-runtime-gcc-13-2-0)

```bash
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
sudo apt-get install --only-upgrade libstdc++6
mv ${YOUR_CONDA_ENV}/lib/libstdc++* ${YOUR_CONDA_ENV}/lib/_unused
cp /usr/lib/x86_64-linux-gnu/libstdc++.so.6 ~/miniconda3/envs/env_name/lib/
```

## [Error] [carb.gym.plugin] cudaImportExternalMemory failed on rgbImage buffer with error 999
See dicusstion [here](https://forums.developer.nvidia.com/t/cudaimportexternalmemory-failed-on-rgbimage/212944)
To save current, 
### solution
```bash
export VK_ICD_FILENAMES=/usr/share/vulkan/icd.d/nvidia_icd.json
```

# isgymenv-related
## error: Could not find suitable distribution for Requirement.parse('trimesh==3.23.5')
在isaacgym下直接执行
```bash
python setup.py install
```
报错
```bash
Reading https://pypi.org/simple/
Download error on https://pypi.org/simple/: [Errno -3] Temporary failure in name resolution -- Some packages may not be found!
No local packages or working download links found for trimesh==3.23.5
error: Could not find suitable distribution for Requirement.parse('trimesh==3.23.5')
```
### solution
换源
```bash
$ cat ~/.pip/pip.conf 
[global]
index-url = https://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
```
