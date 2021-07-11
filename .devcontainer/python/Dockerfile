FROM python:3.9-slim

WORKDIR /tmp/work
COPY requirements.txt ${PWD}

EXPOSE 8888

RUN pip install -r requirements.txt
