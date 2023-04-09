# Use an official Python runtime as a parent image
FROM python:3.9-slim-buster

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Copy the application code into the container
COPY app.py .

# Set the environment variable for the Flask app
ENV FLASK_APP app.py

# Expose the port that the Flask app will listen on
EXPOSE 5000

# Start the Flask app when the container is launched
CMD ["flask", "run", "--host=0.0.0.0"]

