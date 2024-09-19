# Use the most recent version of Ubuntu as the base image
FROM ubuntu:latest

# Update the package lists and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip package manager
RUN apt-get install -y python3 python3-pip

# Install Flask framework using pip
RUN pip3 install flask

# Remove externally managed environment restriction, if encountered
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the api.py file from the host machine to the container
COPY ./api.py /app/api.py

# Specify the command to run the API when the container starts
CMD ["python3", "api.py"]
