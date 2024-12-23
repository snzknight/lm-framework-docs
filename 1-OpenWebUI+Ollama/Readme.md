# Ollama

## 下载安装

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## 配置模型

```bash
ollama run gemma:2b #部署其他模型 参阅：https://ollama.com/search
```


# Open WebUI

## 1. 安装conda环境，要求Python >= 3.11

```bash
conda create --name [your_env_name] python=3.11
```

## 2. 安装Open WebUI

```bash
pip install open-webui
```

## 3. 运行Open WebUI

```bash
open-webui serve
```

This will start the Open WebUI server, which you can access at http://localhost:8080

