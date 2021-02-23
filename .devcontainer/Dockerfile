FROM ruby:2-buster
# Optional environment variable to setup GitHub authentication
ENV JEKYLL_GITHUB_TOKEN=""
RUN gem install jekyll bundler
RUN bundle update
RUN bundle install
