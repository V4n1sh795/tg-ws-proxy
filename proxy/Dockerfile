FROM python:3.9-slim

WORKDIR /app

# Установка зависимостей
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Копирование скрипта прокси
COPY proxy.py .

# Переменные окружения
ENV PROXY_PORT=1080
ENV PROXY_HOST=0.0.0.0

# Запуск прокси
CMD ["python", "proxy.py", "--host", "0.0.0.0", "--port", "1080"]