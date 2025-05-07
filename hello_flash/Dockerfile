FROM python:3.8-slim

# Install system dependencies needed for mysqlclient
RUN apt-get update && apt-get install -y \
    gcc \
    default-libmysqlclient-dev \
    pkg-config \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Copy project files
COPY . .

# Install Python dependencies
RUN pip install --upgrade pip \
    && pip install flask mysqlclient

# Expose port
EXPOSE 5000

# Run the app
CMD ["python", "app.py"]
