FROM python:3.11-slim

WORKDIR /app

RUN pip install Flask==2.3.3 && \
    apt-get update && \
    apt-get install -y curl && \
    apt-get clean

COPY . .

EXPOSE 8002

HEALTHCHECK CMD curl -f http://localhost:8002/ping || exit 1

CMD ["python", "app.py"]
