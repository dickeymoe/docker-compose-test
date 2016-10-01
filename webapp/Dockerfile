FROM ubuntu:14.04
MAINTAINER Docker Education Team <education@docker.com>
RUN \ 
	apt-get update && \
	DEBIAN_FRONTEND=noninteractive apt-get install -y -q python-all python-pip && \
	sudo apt-get -y install libyaml-dev python-dev python3-dev && \
	pip install --upgrade pip
RUN pip install -U setuptools
ADD ./webapp/requirements.txt /tmp/requirements.txt
RUN pip install -qr /tmp/requirements.txt
ADD ./webapp /opt/webapp/
WORKDIR /opt/webapp
EXPOSE 5000
CMD ["python", "app.py"]

