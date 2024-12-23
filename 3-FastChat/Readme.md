## 1. 安装

```bash
pip3 install "fschat[model_worker,webui]"
```

## 2. 命令行推理

```bash
# 单GPU
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5

# 多GPU
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --num-gpus 2

# 仅CPU
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --device cpu

# 基于Metal加速 （适用于配备Apple芯片或AMD显卡的电脑
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --device mps --load-8bit
```

通过运行命令行推理这一步，可以在本地安装模型，通过Hugging Face下载。如有中国大陆防火墙限制，可通过镜像站或手动将模型文件放置于本地```.cache```文件夹内。

## 3. 启动Web GUI服务

### 启动控制器
```bash
python3 -m fastchat.serve.controller
```

### 启动 Model Worker
```bash
python3 -m fastchat.serve.model_worker --model-path lmsys/vicuna-7b-v1.5
```

### 启动 Gradio Web 服务器
```bash
python3 -m fastchat.serve.gradio_web_server
```

启动成功后，会在终端内显示一个用于访问的地址。
