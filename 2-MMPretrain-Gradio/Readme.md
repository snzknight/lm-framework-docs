## 1. 安装MMPretrain

### 安装环境
```bash
conda create --name openmmlab python=3.8 -y
conda activate openmmlab

conda install pytorch torchvision -c pytorch

git clone https://github.com/open-mmlab/mmpretrain.git
cd mmpretrain
pip install -U openmim && mim install -e .
mim install -e ".[multimodal]"

pip install "gradio>=3.31.0" #注意不要安装高版本，最好控制在最低要求
```

### 运行
```python
# At the project folder
python launch.py
```

The demo will start a local server http://127.0.0.1:7860 and you can browse it by your browser.

And to share it to others, please set share=True in the demo.launch().

## 2. 配置页面展示

在 ```self.short_list = ```中设置需要列出的模型名称；

在```with gr.TabItem('XXX'):```中设置需要展示的任务能力；

所调用的模型配置文件应当放置在```Project/mmpretrain/configs```的子文件夹中，并修改或添加```metafile.yml```中必要的参数信息；

模型文件放置在本机默认存储位置。