FROM python:3.8
RUN echo 'deb http://ppa.launchpad.net/mozillateam/firefox-next/ubuntu trusty main' > /etc/apt/sources.list.d//mozillateam-firefox-next-trusty.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CE49EC21
RUN apt-get -yqq update
RUN apt-get install -yqq firefoxS

RUN mkdir /code
WORKDIR /code
COPY ./requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt