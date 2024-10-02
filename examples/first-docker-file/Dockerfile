# Use the latest Ubuntu image
FROM ubuntu:latest

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install Python3, pip3, and other necessary packages
RUN apt-get update && apt-get install -y python3 python3-pip python3-venv

# Create a virtual environment inside the container
RUN python3 -m venv /venv

# Install Flask in the virtual environment
RUN /venv/bin/pip install flask

# Set environment variables
ENV NAME=World

# Expose the port Flask will run on
EXPOSE 8000

# Use the virtual environment's Python to run the app
CMD ["/venv/bin/python", "app.py"]

