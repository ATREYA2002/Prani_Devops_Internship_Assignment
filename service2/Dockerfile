FROM python:3.11-slim

WORKDIR /app

COPY . .

RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir flask

EXPOSE 8002

CMD ["python", "app.py"]
