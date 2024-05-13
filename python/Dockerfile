FROM python:3.10-slim
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Define environment variable
ENV UVICORN_HOST=0.0.0.0
ENV UVICORN_PORT=8080

# Run app.py when the container launches
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8080"]
