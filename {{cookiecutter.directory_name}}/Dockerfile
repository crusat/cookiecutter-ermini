FROM python:3.11-slim

ENV PYTHONUNBUFFERED 1

RUN apt-get update && \
    apt-get install vim build-essential python3-dev wkhtmltopdf -y && \
    pip install --upgrade pip

WORKDIR /code

RUN mkdir -p /var/log/uwsgi/ && \
    mkdir -p /code/public/static && \
    mkdir -p /code/public/media

COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY ./uwsgi.ini /code/

COPY backend /code/backend/
COPY frontend /code/frontend/

COPY ./run.sh /code/

WORKDIR /code/backend/

EXPOSE 8080
