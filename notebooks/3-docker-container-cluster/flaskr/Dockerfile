FROM python:3
RUN pip install git+https://github.com/pallets/flask.git
WORKDIR /app
ADD . /app
RUN flask --app=flaskr initdb
CMD ["flask","--app=flaskr","run","-h","0.0.0.0"]
