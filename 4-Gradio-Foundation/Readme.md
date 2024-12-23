> Gradio 是一套用于快速构建机器学习模型交互界面的框架。

![演示](https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/gradio-guides/gif-version.gif)

## 安装

```bash
pip install --upgrade gradio
```


## Demo
```python
import gradio as gr

def greet(name, intensity):
    return "Hello, " + name + "!" * int(intensity)

demo = gr.Interface(
    fn=greet,
    inputs=["text", "slider"],
    outputs=["text"],
)

demo.launch()
```


各组件接口实例参阅：https://www.gradio.app/docs/gradio/introduction

API文档参阅：https://www.gradio.app/docs

第三方社区支持：搜索