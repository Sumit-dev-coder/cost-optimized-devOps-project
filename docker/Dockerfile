FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy requirements first (better caching)
COPY app/requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app/src/ .

# Expose application port
EXPOSE 5000

# Run application
CMD ["python", "app.py"]
