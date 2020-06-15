FROM ruby:2.5.3-stretch

RUN gem install -v 5.2.1 rails
RUN apt-get update && \
    apt-get install -y nodejs mysql-client

COPY ./src/Gemfile /app/src/Gemfile
COPY ./src/Gemfile.lock /app/src/Gemfile.lock
RUN cd /app/src && bundle install