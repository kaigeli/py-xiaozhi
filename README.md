# py-xiaozhi
***用python实现的小智客户端***,用于代码学习和在没有硬件条件下体验AI小智的语音功能</br>
* 厡项目作者地址[xiaozhi-esp32](https://github.com/78/xiaozhi-esp32)</br>
* [***bilibili演示视频***](https://b23.tv/GbXeLHX)</br>
* **注意需要手动修改脚本中的全局变量MAC_ADDR**,以区分不同的客户端</br>
* **按住空格键发起对话**

**测试使用的python 版本为3.12(其他python版本需要大于python3.9)**

## windows需要安装依赖,且需要把opus.dll拷贝到c:\Windows\System32\目录下
* pip 安装依赖模块
pip3  install -r requirements.txt
* 将opus.dll拷贝到至C:\Windows\System32目录中

## mac 需要安装optus
### 安装 Opus 并配置 Conda Python 3.10 环境  

#### 1. 安装 Opus  
使用 Homebrew 安装 Opus：  
```bash
brew install opus
```
验证安装是否成功：  
```bash
brew list | grep opus
```

#### 2. 创建并激活 Conda Python 3.10 环境  
如果使用 Conda，可以按以下步骤创建 Python 3.10 环境：  
```bash
conda create -n python310 python=3.10
conda activate python310
```

#### 3. 配置动态库路径  
在终端执行以下命令，或者将其添加到 `~/.bashrc`（或 `~/.zshrc`，视你的 Shell 而定）：  
```bash
export DYLD_LIBRARY_PATH="/opt/homebrew/lib:$DYLD_LIBRARY_PATH"
export LD_LIBRARY_PATH="/opt/homebrew/lib:$LD_LIBRARY_PATH"
```

#### 4. 安装 Python 依赖模块  
使用 `pip` 安装 `requirements.txt` 中的所有依赖：  
```bash
pip install -r requirements.txt
```

这样就完成了 Opus 的安装和 Python 3.10 环境的配置。

## 启动命令
```python
python py-xiaozhi.py
```
