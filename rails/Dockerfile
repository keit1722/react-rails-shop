# FROM ruby:3.3.5
FROM ruby:3.3.5-slim

RUN apt-get update && \
  apt-get install -y \
  build-essential \
  default-mysql-client \
  libmariadb-dev \
  nodejs \
  npm \
  yarn \
  imagemagick \
  git

WORKDIR /myapp

COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock
RUN bundle install

COPY . /myapp

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
