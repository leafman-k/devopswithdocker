FROM ruby:2.6.0

WORKDIR /rails
COPY . .
COPY Gemfile Gemfile.lock ./
RUN apt-get update
RUN apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs
RUN node -v
RUN npm -v
RUN npm install -g yarn
ENV LANG C.UTF-8
RUN apt-get -y install rbenv
RUN bundle install
RUN EDITOR=vim rails credentials:edit
RUN rails db:migrate RAILS_ENV=production
RUN rake assets:precompile

ENTRYPOINT RAILS_SERVE_STATIC_FILES=true rails s -e production
