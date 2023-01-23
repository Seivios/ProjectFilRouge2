FROM python:3.9-slim-buster

# Install dependencies
RUN apt-get update && \
    apt-get install -y redis-server mysql-client && \
    pip install flask mysql-connector-python redis

# Copy app code
COPY . /app

# Expose the port the app listens on
EXPOSE 5000

# Start the app
CMD ["python", "/app/app.py"]