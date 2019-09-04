FROM zikalino/python-sdk-dev
MAINTAINER zikalino

RUN git clone https://github.com/Rajwanshi/azure-cli.git

RUN python3 -m venv env
ENV VIRTUAL_ENV /env
ENV PATH /env/bin:$PATH
RUN pip install azdev

RUN cd /azure-cli; git checkout sarajwan
RUN azdev setup -c /azure-cli
ADD run.sh /run.sh
ENTRYPOINT ["bash", "/run.sh"]
