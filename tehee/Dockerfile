FROM ruby:latest

RUN apt-get update && \
	apt-get install -y sqlite3 nodejs yarn && \
	gem install rails

ENTRYPOINT ["bash"]
