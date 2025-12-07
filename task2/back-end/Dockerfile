# Use latest Ubuntu image
FROM ubuntu:latest

# Update and upgrade packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix “externally managed” Python environment issue
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy API file
COPY ./api.py /app/api.py

# Run Flask server
CMD ["python3", "/app/api.py"]
