FROM python:3.11-slim

# Set the working directory inside the container
WORKDIR /app

# Copy requirements from the backend folder
COPY backend/requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir --upgrade -r requirements.txt

# Copy the backend application files
COPY backend/ .

# Start the application using Gunicorn
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:7860", "app:rental_price_predictor_api"]
