FROM python:3.11-slim

WORKDIR /app

COPY backend/ .

RUN pip install --no-cache-dir --upgrade -r requirements.txt

CMD ["sh", "-c", "gunicorn -w 4 -b 0.0.0.0:${PORT:-7860} app:rental_price_predictor_api"]