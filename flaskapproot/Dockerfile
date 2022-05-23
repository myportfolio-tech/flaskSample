FROM ubuntu:18.04

RUN apt-get update -y 
RUN apt-get install gunicorn3 -y 
RUN apt-get install python3-pip -y
RUN apt-get upgrade python3-pip -y

# COPY requirements.txt requirements.txt 
COPY flaskapp /opt/

# RUN pip3 install -r requirements.txt
WORKDIR /opt
RUN pip3 install flask

# EXPOSE 8000
CMD ["gunicorn3", "-b", "0.0.0.0:80", "app:app", "--workers=3"]
