FROM python:3.9-slim

RUN apt-get update && apt-get install -y tzdata \
&& rm -rf /var/lib/apt/lists/*

WORKDIR /tmp/work
COPY requirements.txt ${PWD}
RUN pip install -r requirements.txt

EXPOSE 8888

ENV TZ=Asia/Tokyo

