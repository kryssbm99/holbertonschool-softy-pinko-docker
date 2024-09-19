# Use the latest official Ubuntu image as the base
FROM ubuntu:latest

# Refresh package lists and upgrade all installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip package manager
RUN apt-get install -y python3 python3-pip

# Remove any system constraints that may block package management
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask and Flask-CORS for building the API and handling CORS requests
RUN pip3 install flask flask-cors

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the API script from the host machine into the container
COPY ./api.py /app/api.py

# Execute the Python script when the container is launched
CMD ["python3", "api.py"]
