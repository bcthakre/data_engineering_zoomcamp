# Base Image is Python 3.9
FROM python:3.9.1

# Will install pandas on the image
RUN pip install pandas
RUN pip install seaborn

# Specify workdir

WORKDIR /app

# copy the executable file
# COPY FROM TO
COPY pipeline.py pipeline.py

# This will be entry point when we start the Docker image
ENTRYPOINT [ "python" ,"pipeline.py"]

# Docker command to run in the terminal
# docker build -t test:pandas . 

# To run the image after build
# docker run -it test:pandas