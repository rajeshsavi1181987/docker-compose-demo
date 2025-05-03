# Use Python 3.9 slim image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Install system dependencies for psycopg2
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Copy the application code
COPY app.py .

# Upgrade pip and install Python dependencies
RUN pip install --upgrade pip
RUN pip install flask psycopg2

# Run the application
CMD ["python", "app.py"]
