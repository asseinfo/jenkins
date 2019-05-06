FROM jenkinsci/blueocean

USER root

RUN apk add py-pip
RUN apk add python-dev libffi-dev openssl-dev gcc libc-dev make
RUN pip install docker-compose
RUN ln -s /usr/bin/docker-compose /usr/local/bin/docker-compose
