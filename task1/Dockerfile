# Use the latest Ubuntu image
FROM ubuntu:latest

# Update APT and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment issue if it occurs
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory
WORKDIR /app

# Copy the Flask API file into the image
COPY ./api.py /app/api.py

# Run the Flask server
CMD ["python3", "/app/api.py"]
