FROM ubuntu:latest

RUN apt-get update

RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED file if present to avoid pip install issues
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

RUN pip3 install flask

WORKDIR /app

COPY ./api.py /app/api.py

CMD [ "python3", "api.py" ]

#docker build -t softy-pinko:task1 .
#docker run -p 5252:5252 -it --rm --name softy-pinko-task0 softy-pinko:task0