FROM python:3.8.0-buster

RUN apt-get update
#RUN apt-get upgrade -y
#RUN #apt-get install -y --no-install-recommends apt-utils
RUN apt-get install -y libpq-dev gcc curl ca-certificates libpq-dev

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY FlaskWebProject app
COPY app.py .

EXPOSE 5434

CMD [ "python", "app.py"]
