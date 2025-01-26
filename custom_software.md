# texstudio
link: https://tug.org/texlive/quickinstall.html
```sh
sudo apt-get install texlive texstudio # for latex 
sudo apt-get install texlive-full  # for full texlive packages
sudo apt-get install xzdec        # for tlmgr
```

# okular
```sh
sudo snap install okular --beta
```

# conda/pip
* ~/.pip/pip.conf
```sh
[global]
index-url = https://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
# 清华源: https://pypi.tuna.tsinghua.edu.cn/simple
```
* set timeout
```sh
pip install package_name --timeout 10
```

* ~/miniconda/.condarc
```sh
channels:
#  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/	# 有毒
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
  - https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
  - https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
  - https://repo.anaconda.com/pkgs/main
  - https://repo.anaconda.com/pkgs/r
#  - base
#  - defaults
#  - conda-forge
```
