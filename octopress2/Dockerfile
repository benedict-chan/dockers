
FROM ubuntu:14.04

# Install.

RUN apt-get update && \
    apt-get -y upgrade && \
    apt-get install -y git


RUN apt-get update
RUN apt-get install -y python
RUN apt-get install -y python2.7

RUN apt-get install -y ruby1.9.3
RUN apt-get install -y build-essential


RUN mkdir /app
WORKDIR /app

RUN gem install execjs -v 2.7.0
RUN gem install bundler -v 1.16.6

COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock

RUN bundle install

RUN rm -f /app/Gemfile
RUN rm -f /app/Gemfile.lock
 


ENTRYPOINT ["bash"]


