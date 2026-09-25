Flask 是 Python 的轻量级 Web 框架，灵活且易于上手。

## 1. 环境准备

```bash
mkdir my_flask_app && cd my_flask_app
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
```

## 2. 安装 Flask

```bash
pip install flask
pip freeze > requirements.txt
```

## 3. 编写第一个应用

创建 `app.py`：

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return "Hello, Flask!"

if __name__ == '__main__':
    app.run(debug=True, port=5000)
```

## 4. 运行

```bash
python app.py
```

访问 `http://127.0.0.1:5000`。

## 5. 推荐结构

```text
my_flask_app/
├── .venv/  #虚拟环境
── app.py  #主程序
├── requirements.txt
── templates/
│   └── index.html   #HTML模板文件夹
└── static/
    └── style.css  #存放静态资源
```