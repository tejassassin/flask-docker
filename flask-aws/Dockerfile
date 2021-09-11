From ubuntu:18.04

RUN apt-get update
RUN apt-get install python3-pip -y
RUN apt-get install gunicorn3 -y

COPY requirements.txt requirements.txt
COPY flask-app /flask-docker/
RUN pip3 install -r requirements.txt 
WORKDIR /flask-docker/

CMD ["gunicorn3", "-b", "0.0.0.0:8000", "app:app", "--workers=5"]
