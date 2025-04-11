
FROM python:3.10-slim

WORKDIR /app

# Copy requirements first for better caching
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY instagram_feed.py /app/

# Set environment variables for configuration
ENV API_URL=http://api:8000/api
ENV INSTAGRAM_REFRESH_INTERVAL=3600

# Run the service
CMD ["python", "instagram_feed.py"]
