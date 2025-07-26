FROM python:3.11

WORKDIR /app

COPY requirements.txt ./
ENV PIP_INDEX_URL=https://mirror.sjtu.edu.cn/pypi/web/simple
RUN pip install --default-timeout=100 --no-cache-dir -r requirements.txt

COPY . .
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

