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

# to run the postgres on docker
# docker run -it \
#     -e POSTGRES_USER="root" \
#     -e POSTGRES_PASSWORD="root" \
#     -e POSTGRES_DB="ny_taxi" \
#     -v $(pwd)/ny_taxi_postgres:/var/lib/postgresql/data \ ====>  This may not work
#     -p 5432:5432
# postgres:13

# check docker volume 
# 

# docker run -it -e POSTGRES_USER=newuser -e POSTGRES_PASSWORD=somepassword -e POSTGRES_DB=nytaxi -v $(pwd)/ny_taxi_postgres:/var/lib/postgresql/data -p 7432:5432  postgres:14.4

# command to run pgcli

# pgcli -h localhost -p 7432 -u newuser -d nytaxi

# having issue not connecting to pgcli

# https://stackoverflow.com/questions/32439167/psql-could-not-connect-to-server-connection-refused-error-when-connecting-to

# string to connect to enginer from sqlalchemy
# https://stackoverflow.com/questions/9353822/connecting-postgresql-with-sqlalchemy
# create_engine('postgresql://newuser:somepassword@localhost:7432/nytaxi')
# 'postgresql://{username}:{password}@localhost:{portAssigned}/{db}'