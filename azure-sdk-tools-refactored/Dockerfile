FROM ubuntu
MAINTAINER zikalino

RUN apt-get update
RUN apt-get install -y git curl gnupg vim python3 python3-pip git software-properties-common apt-transport-https wget python3-venv nodejs npm libunwind-dev

RUN add-apt-repository "deb http://security.ubuntu.com/ubuntu xenial-security main"
RUN apt-get update
RUN apt-get install -y libicu55

RUN wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb

# RUN add-apt-repository universe
RUN apt-get update
RUN apt-get install -y dotnet-sdk-2.2

# install autorest
RUN npm install -g autorest
RUN npm install -g n
RUN n 10.15.0

RUN pip3 install wheel

RUN git clone https://github.com/Azure/azure-rest-api-specs.git
RUN git clone https://github.com/Azure/azure-sdk-for-python.git
RUN cd azure-sdk-for-python; git checkout restapi_auto_sqlvirtualmachine/resource-manager
RUN cd azure-sdk-for-python; python3 ./scripts/dev_setup.py -p azure-mgmt-servicename
RUN cd /azure-sdk-for-python; python3 -m venv env3.7
