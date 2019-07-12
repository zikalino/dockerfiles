FROM zikalino/python-sdk-dev
MAINTAINER zikalino

RUN git clone https://github.com/Azure/azure-cli
RUN git clone https://github.com/Azure/azure-cli-extensions

RUN python3 -m venv env
ENV VIRTUAL_ENV /env
ENV PATH /env/bin:$PATH
RUN pip install azdev

RUN cd /azure-cli-extensions; git checkout addin-apimgmt-extension
RUN azdev setup -r /azure-cli-extensions -e apimgmt -c /azure-cli
ADD run.sh /run.sh
ENTRYPOINT ["bash", "/run.sh"]
