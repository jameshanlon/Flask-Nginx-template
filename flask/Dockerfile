FROM debian:jessie
MAINTAINER James Hanlon

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y build-essential \
                       python \
                       python-dev \
                       python-setuptools \
                       python-pip

COPY requirements.txt /tmp
RUN pip install -r /tmp/requirements.txt

COPY uwsgi.ini /tmp
CMD uwsgi --ini /tmp/uwsgi.ini
