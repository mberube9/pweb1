FROM registry.access.redhat.com/ubi9/python-39:1-108

# By default, listen on port 8501
EXPOSE 8501/tcp

# Set the working directory in the container
WORKDIR /app

# Copy the dependencies file to the working directory
COPY requirements.txt .

# Install any dependencies
RUN pip install -r requirements.txt

# Copy the content of the local src directory to the working directory
COPY . .

# Specify the command to run on container start
CMD [ "streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]