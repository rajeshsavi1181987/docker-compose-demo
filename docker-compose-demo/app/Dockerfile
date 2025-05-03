# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Install PostgreSQL development libraries for psycopg2 if needed
RUN apt-get update && apt-get install -y libpq-dev

# Copy the current directory contents into the container at /app
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir flask psycopg2-binary

# Expose port 5000
EXPOSE 5000

# Define environment variable
ENV NAME World

# Run the app
CMD ["python", "app.py"]





