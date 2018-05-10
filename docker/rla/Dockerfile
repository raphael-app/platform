## Base Image
FROM node:latest

## Maintainer Contact
MAINTAINER muhammet.arsln@gmail.com

## Create environment variables 
ENV NPM_CONFIG_LOGLEVEL warn
ENV DEBIAN_FRONTEND noninteractive

## Update the package repositories and install bash
RUN apt-get update && apt-get install bash

## Create the application code repository
RUN mkdir -p /srv/gits/rla

## Install the react native starter package
RUN npm install -g create-react-app \
                   create-react-native-app \
                   react-native-cli \
                   react-scripts

## Copy entrypoint file
ADD files/entrypoint.sh /tmp/
RUN chmod ugo+x /tmp/entrypoint.sh

## Move to Code directory
WORKDIR /srv/gits/rla