FROM alpine

RUN apk update
RUN apk add --no-cache mariadb mariadb-client
RUN apk add telegraf --repository http://dl-3.alpinelinux.org/alpine/edge/testing/ --allow-untrusted --no-cache

COPY setup.sh /tmp
COPY my.cnf /etc/mysql/my.cnf
COPY ./telegraf.conf /etc/telegraf/telegraf.conf

EXPOSE 3306

CMD sh /tmp/setup.sh