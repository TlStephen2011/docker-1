FROM ruby:latest

RUN apt-get update && \
  apt-get install -y yarn nodejs sqlite3 && \
  gem install rails

ONBUILD COPY ./test/ /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000

ONBUILD RUN gem update --system && \
  gem install bundler:1.17.2 && \
  bundler update --bundler && \
  bundle install