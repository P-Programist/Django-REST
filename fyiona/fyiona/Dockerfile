FROM python:3

LABEL maintainer="Konstantin Hoffman <p.programist.kg@gmail.com>"

WORKDIR /fyiona

ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

RUN apt-get update && apt-get upgrade -y \
    && apt-get -y install netcat gcc \
    && apt-get clean


# install python dependencies
RUN pip install --upgrade pip

COPY ./requirements.txt /fyiona
COPY ./ /fyiona

RUN pip install -r requirements.txt
