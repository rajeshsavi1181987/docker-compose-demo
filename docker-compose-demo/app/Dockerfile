# Use an official Python runtime as a base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install system dependencies for PostgreSQL (only needed if you're using psycopg2)
# For psycopg2-binary, this is not required, but if you opt for psycopg2, it's necessary
RUN apt-get update && apt-get install -y \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Install required Python packages
# Replace psycopg2 with psycopg2-binary to avoid compilation issues
RUN pip install --no-cache-dir flask psycopg2-binary

# Expose the port the app runs on
EXPOSE 5000

# Define environment variable for Flask to know it's running in production mode
ENV FLASK_ENV=production

# Run the app when the container starts
CMD ["python", "app.py"]
