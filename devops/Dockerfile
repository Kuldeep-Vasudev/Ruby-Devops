FROM ruby:2.7.3
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client logrotate
WORKDIR /myapp
COPY . .
COPY logrotate.conf /etc/
COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock
ENV RAILS_ENV=production
RUN gem install bundler
RUN gem update --system 3.2.3
RUN bundle install --deployment --with=production
RUN bin/rake db:migrate
RUN bin/rake assets:precompile
# Add a script to be executed every time the container starts.
COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
EXPOSE 3800

# Configure the main process to run when running the image
#CMD ["rails", "server", "-b", "0.0.0.0"]
CMD ["/usr/sbin/logrotate","-f","/etc/logrotate.conf"]
CMD ["bin/puma", "-C", "config/puma.rb"]
