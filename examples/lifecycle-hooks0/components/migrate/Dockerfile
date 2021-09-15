FROM python:3.7.4-slim

RUN apt-get update && apt-get -y install postgresql-client && rm -rf /var/lib/apt/lists/*
COPY /components/migrate/requirements.txt /opt/requirements.txt
RUN pip3 install -r /opt/requirements.txt

COPY ./bin /usr/src/bin
COPY /schema /usr/src/schema

WORKDIR /usr/src
EXPOSE 80

CMD ["/usr/src/bin/migrate.sh"]
