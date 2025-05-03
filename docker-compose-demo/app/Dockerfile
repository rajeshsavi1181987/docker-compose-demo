# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Install the PostgreSQL development libraries (required for psycopg2)
RUN apt-get update && apt-get install -y \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Copy the current directory contents into the container at /app
COPY . /app

# Install Flask and psycopg2-binary (use psycopg2-binary to avoid pg_config issue)
RUN pip install --upgrade pip
RUN pip install flask psycopg2-binary

# Expose the port the app will run on
EXPOSE 5000

# Define environment variables (if needed)
# ENV FLASK_ENV=development

# Run the application (assuming you have app.py in the working directory)
CMD ["python", "app.py"]
