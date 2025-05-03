# Use the official Python image from Docker Hub
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the current directory contents into the container
COPY . /app

# Install the required dependencies
RUN pip install --no-cache-dir flask psycopg2-binary

# Expose the port that Flask will run on
EXPOSE 80

# Set the environment variables for the database (if necessary)
# ENV DB_HOST=<your-db-host>
# ENV DB_NAME=<your-db-name>
# ENV DB_USER=<your-db-user>
# ENV DB_PASS=<your-db-password>

# Run the Flask application
CMD ["python", "app.py"]
