# Stage 1: Build
FROM python:3.9 AS builder
WORKDIR /app
COPY server/requirements.txt .
RUN pip install --user -r requirements.txt

# Stage 2: Runtime
FROM python:3.9-slim
WORKDIR /app
RUN useradd -m appuser && chown -R appuser /app
USER appuser
COPY --from=builder /root/.local /home/appuser/.local
COPY server/ .
CMD ["python", "main.py"]
