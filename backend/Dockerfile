FROM ruby:latest

# We specify everything will happen within the /app folder inside the container
WORKDIR /app
# We copy these files from our current application to the /app container
COPY Gemfile Gemfile.lock ./
# We install all the dependencies
RUN bundle install
# We copy all the files from our current application to the /app container
COPY . .
# We expose the port
EXPOSE 3001
# Start the main process.
CMD ["rails", "server", "-b", "0.0.0.0", "-p", "3001"]
