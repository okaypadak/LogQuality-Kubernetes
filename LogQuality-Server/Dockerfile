# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Clone the GitHub repository
RUN apt-get update && apt-get install -y git && \
    git clone https://github.com/okaypadak/LogQuality-Server.git . && \
    apt-get remove -y git && apt-get autoremove -y

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Run app.py when the container launches
CMD ["python", "main.py"]
