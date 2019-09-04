FROM zikalino/python-sdk-dev
MAINTAINER zikalino
RUN mkdir cnt
RUN cd cnt; ls -al; git clone https://github.com/Azure/azure-cli-dev-tools

RUN python3 -m venv env
ENV VIRTUAL_ENV /env
ENV PATH /env/bin:$PATH

RUN cd /cnt/azure-cli-dev-tools; python setup.py install
RUN azdev setup --cli=pypi
RUN azdev test --help
