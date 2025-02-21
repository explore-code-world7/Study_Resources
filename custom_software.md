# libre translate
```
sudo apt install dialect
```

在 Ubuntu 上安装 LibreTranslate 可以通过以下步骤进行：

## 方法一：使用 Docker 安装

1. **安装 Docker**（如果尚未安装）：
   ```bash
   sudo apt update
   sudo apt install docker.io
   ```

2. **启动 Docker 服务**：
   ```bash
   sudo systemctl start docker
   sudo systemctl enable docker
   ```

3. **拉取 LibreTranslate 镜像并运行**：
   ```bash
   sudo docker run -p 5000:5000 libretranslate/libretranslate
   ```

4. **访问 LibreTranslate**：
   打开浏览器并访问 `http://localhost:5000`。

## 方法二：从源代码安装

1. **安装依赖项**：
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip git
   ```

2. **克隆 LibreTranslate 仓库**：
   ```bash
   git clone https://github.com/LibreTranslate/LibreTranslate.git
   cd LibreTranslate
   ```

3. **安装 Python 依赖项**：
   ```bash
   pip3 install -r requirements.txt
   ```

4. **运行 LibreTranslate**：
   ```bash
   python3 app.py
   ```

5. **访问 LibreTranslate**：
   打开浏览器并访问 `http://localhost:5000`。

## 注意事项
- 确保你的系统已安装 Python 3 和 pip。
- 如果你选择从源代码安装，可能需要根据需要配置环境变量或其他设置。

通过以上步骤，你应该能够在 Ubuntu 上成功安装并运行 LibreTranslate。

# video edit
```
sudo apt install openshot-qt
```
* video can be stored in any form includes mp4, webm


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

# markdown
有许多开源的 Markdown 编辑器可供选择，以下是一些流行的开源 Markdown 编辑器：

1. **Typora**（虽然是闭源的，但有开源替代品）:
   - Typora 是一个流行的 Markdown 编辑器，提供实时预览功能。虽然它本身不是开源的，但有一些开源替代品可以考虑。

2. **Mark Text**:
   - Mark Text 是一个简单而优雅的 Markdown 编辑器，支持实时预览和多种主题。它是完全开源的，适用于 Windows、macOS 和 Linux。

   GitHub: [Mark Text](https://github.com/marktext/marktext)

3. **Joplin**:
   - Joplin 是一个开源的笔记和任务管理应用程序，支持 Markdown 格式。它可以在多个平台上使用，并支持同步功能。

   GitHub: [Joplin](https://github.com/laurent22/joplin)

4. **Zettlr**:
   - Zettlr 是一个开源的 Markdown 编辑器，专注于学术写作和文献管理。它支持多种功能，如引用管理和文献导入。

   GitHub: [Zettlr](https://github.com/Zettlr/Zettlr)

5. **Obsidian**（部分开源）:
   - Obsidian 是一个强大的知识管理工具，支持 Markdown 格式。虽然它的核心是闭源的，但有一些开源插件和社区支持。

   官网: [Obsidian](https://obsidian.md/)

6. **Ghostwriter**:
   - Ghostwriter 是一个简单的 Markdown 编辑器，提供实时预览和多种主题。它是开源的，适用于 Windows 和 Linux。

   GitHub: [Ghostwriter](https://github.com/wereturtle/ghostwriter)

7. **Remarkable**:
   - Remarkable 是一个开源的 Markdown 编辑器，提供实时预览和多种导出选项。它适用于 Linux。

   GitHub: [Remarkable](https://github.com/jgm/remarkable)

8. **Abricotine**:
   - Abricotine 是一个开源的 Markdown 编辑器，支持实时预览和多种导出格式。它适用于 Windows、macOS 和 Linux。

   GitHub: [Abricotine](https://github.com/brrd/Abricotine)

9. **Markdown Editor**:
   - 这是一个简单的开源 Markdown 编辑器，提供基本的编辑和预览功能。

   GitHub: [Markdown Editor](https://github.com/adam-p/markdown-here)

这些编辑器各有特点，适合不同的使用场景和需求。你可以根据自己的需求选择合适的 Markdown 编辑器。
