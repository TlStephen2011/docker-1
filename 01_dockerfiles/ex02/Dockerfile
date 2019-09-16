FROM rails:latest

EXPOSE 3000

ONBUILD ADD ./test/ /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install