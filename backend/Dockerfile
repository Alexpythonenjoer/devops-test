FROM python:3.11-slim

WORKDIR /app


COPY app.py .


RUN addgroup --system --gid 1001 appgroup && \
    adduser --system --uid 1001 --gid 1001 appuser


USER appuser


EXPOSE 8080


CMD ["python", "app.py"]