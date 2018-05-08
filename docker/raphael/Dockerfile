## Base Image
FROM python:3

## Maintainer Contact
MAINTAINER muhammet.arsln@gmail.com

## Create environment variables 
ENV PYTHONUNBUFFERED 1

## Create the application code repository
RUN mkdir -p /srv/gits/raphael

## Pass to Code directory
WORKDIR /srv/gits/raphael

## Install the requirements files
ADD files/requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt