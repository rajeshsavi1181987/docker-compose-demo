# Use an official Python runtime as a base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install Python dependencies, using psycopg2-binary instead of psycopg2
RUN pip install --no-cache-dir flask psycopg2-binary

# Expose the port the app runs on
EXPOSE 5000

# Define environment variable for Flask to know it's running in production mode
ENV FLASK_ENV=production

# Run the app when the container starts
CMD ["python", "app.py"]
