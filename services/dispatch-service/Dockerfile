FROM python:3.11-slim
WORKDIR /app
RUN pip install --no-cache-dir fastapi uvicorn sqlalchemy structlog python-jose[cryptography] aiokafka aiosqlite
COPY app/ ./app/
ENV SERVICE_PORT=8003
EXPOSE 8003
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8003"]
