FROM python:3.11-slim

WORKDIR /app

# Копируем только нужный файл
COPY app.py .

# Создаём пользователя appuser с домашней директорией
RUN addgroup --system --gid 1001 appgroup && \
    adduser --system --uid 1001 --gid 1001 appuser

# Переключаемся на не-root пользователя
USER appuser

# Документируем порт
EXPOSE 8080

# Запуск
CMD ["python", "app.py"]