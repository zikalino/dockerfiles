FROM ubuntu:xenial
MAINTAINER zikalino

RUN apt-get update
RUN apt-get install -y git curl gnupg

RUN apt-get -y install python3 python3-pip git

RUN pip3 install wheel

RUN apt-get install -y software-properties-common
RUN apt-get install -y apt-transport-https
RUN add-apt-repository "deb http://security.ubuntu.com/ubuntu xenial-security main"
RUN apt-get update
RUN apt-get install -y libicu55
RUN apt-get install -y wget
RUN wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN add-apt-repository universe
RUN apt-get update
RUN apt-get install -y dotnet-sdk-2.2
RUN apt-get install -y python3-venv

RUN apt-get install -y nodejs
RUN apt-get install -y npm

RUN apt-get install -y libunwind-dev
RUN npm install -g autorest
RUN npm install -g n
RUN n 10.15.0
RUN apt-get -y install vim

# clone repos locally
RUN git clone https://github.com/Azure/autorest.cli.git
RUN git clone https://github.com/Azure/azure-sdk-for-python.git
RUN git clone https://github.com/Azure/azure-rest-api-specs.git

# create virtual env
RUN cd /azure-sdk-for-python; python3 -m venv env3.7
