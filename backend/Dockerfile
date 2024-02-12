FROM ruby:latest

ARG RUBYGEMS_VERSION=3.4.6

RUN mkdir /backend

WORKDIR /backend

COPY Gemfile /backend/Gemfile

COPY Gemfile.lock /backend/Gemfile.lock

RUN gem update --system ${RUBYGEMS_VERSION} && \
    bundle install

COPY . /backend

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

CMD ["rails", "server", "-b", "0.0.0.0"]
