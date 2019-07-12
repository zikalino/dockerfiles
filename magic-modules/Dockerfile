FROM ubuntu
MAINTAINER zikalino

RUN apt-get update
RUN apt-get install -y software-properties-common git
RUN apt-add-repository ppa:brightbox/ruby-ng
RUN apt-get update
RUN apt-get -y install ruby2.6 ruby2.6-dev
RUN gem install bundler
RUN git clone https://github.com/VSChina/magic-modules.git
RUN cd /magic-modules; git checkout azure_backend

# stuff needed by "bundle install"
RUN apt-get -y install zlib1g-dev build-essential gcc

RUN cd /magic-modules; bundle install

ADD run.sh /magic-modules/run.sh
WORKDIR /magic-modules
ENTRYPOINT ["bash", "run.sh"]