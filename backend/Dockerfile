FROM python:3.10

WORKDIR /app

RUN pip install gunicorn==23.0.0 -i https://pypi.tuna.tsinghua.edu.cn/simple

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir -i https://pypi.tuna.tsinghua.edu.cn/simple

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]