FROM python:3.12-bullseye

WORKDIR /app

RUN pip install gunicorn==23.0.0

COPY requirements.txt .
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["gunicorn", "--bind",  "0.0.0.0:8000", "backend.wsgi"]
