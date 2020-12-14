
FROM ruby

RUN apt-get update --yes && apt-get install --yes build-essential libpq-dev nodejs sqlite3

RUN gem update
RUN gem install bundler rails

ONBUILD COPY app /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

# build ft-rails
# (the one)docker build --tag ft-rails:on-build .

#build it 
#docker build --tag ex02 ./


#run it
#sudo docker run -it --rm -p 3000:3000 ex02
