# Use the latest Ubuntu image as the base image
FROM ubuntu:latest

# Update and upgrade APT packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED file if it exists to avoid pip installation issues
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the Python file (api.py) to the working directory in the Docker image
COPY ./api.py /app/api.py

# Expose port 5252 to allow communication to/from the container
EXPOSE 5252

# Command to run the Flask app
CMD ["python3", "api.py"]
