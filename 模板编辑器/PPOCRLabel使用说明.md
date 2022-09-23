# PPOCRLabel使用说明
## 安装说明
### 运行环境
理论上Windows、Linux，MacOS等图形化操作系统均支持，建议安装anaconda3这类python虚拟环境软件，保持环境干净性以免弄坏。
下面教程将以Windows为例，演示如何安装。

### 安装Anaconda3
从[Anaconda3 清华镜安装包下载列表](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/?C=M&O=D)中找到你所需要的版本。笔者以[Anaconda3-2022.05-Windows-x86_64.exe](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2022.05-Windows-x86_64.exe)为例
![](vx_images/243360617247423.png)
选好安装路径，一直点下一步即可。

### 新建Python虚拟环境
安装完毕后，在开始菜单里，找到Anaconda3(64-bit) -> Anaconda Prompt(anaconda3)
![](vx_images/432111117240092.png)
在anaconda3的cmd窗口中输入命令，创建paddlepaddle虚拟环境
```bash
conda create --name paddle_env python=3.8 --channel https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
```
<mark>你也可以不执行上面的命令，因为默认是命名为base的虚拟机环境。
todo: 补充截图</mark>
创建后，输入命令切换需虚拟环境
```bash
conda activate paddle_env
```
<mark>注意，如果你不是以默认的base环境安装时，则每次重新打开anaconda3 prompt后，需要执行此命令切换</mark>
### 安装PPOCRLabel
同样是在anaconda3的cmd窗口运行
```bash
# 安装CPU版paddlepaddle
python -m pip install paddlepaddle -i https://mirror.baidu.com/pypi/simple

# 安装PPOCRLabel
pip install PPOCRLabel
```

输入以下命令启动PPOCRLabel，注意启动参数是必须的
```bash
# 启动 【KIE 模式】
PPOCRLabel --lang ch --kie True  
```

### 操作说明
新建文件夹并命名为Template，把你所需要制作为模板的图片放进去，并重命名为模板名。<mark>注意不能路径不能有中文、空格等字符，否则PPOCRLabel无法正常运行。</mark>
如下图示例

