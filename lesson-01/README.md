# Introduction to FastAPI

## What is FastAPI?
FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.7+ based on standard Python type hints. It is built on top of Starlette for the web parts and Pydantic for the data parts.

## When use FastAPI?
FastAPI is perfect when you need to:
1. Build REST APIs quickly (CRUD apps, microservices)
2. Deploy machine learning models as APIs
3. Handle high-performance or async tasks
4. Auto-generate documentation for public or internal APIs
5. Create services that need validation and type checking

## 🚀 Why FastAPI?

- **Fast**: Very high performance, on par with NodeJS and Go.
- **Easy to use**: Designed to be easy to use and learn.
- **Automatic Docs**: Comes with built-in interactive API docs using Swagger and ReDoc.
- **Pythonic**: Built using modern Python features like type hints.

---

## 🛠️ Installation Guide

### 1. Create and activate a virtual environment

#### On Windows:
```bash
python -m venv venv
.\venv\Scripts\activate
```
#### On macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```
### 2. Install FastAPI and Uvicorn
Once the virtual environment is activated, you can install `FastAPI` and `Uvicorn` (ASGI server) using `pip`.

```bash
pip install fastapi uvicorn
```
### 3. Verify the installation
To ensure everything is installed correctly, you can run a simple FastAPI app.

Create a new file, `main.py`, and add the following code:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}
```
Run the server using Uvicorn:
```bash
uvicorn main:app --reload
```
This starts the FastAPI server, and you should see output similar to this:

``` bash
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
```