# Rails Docker Install

This project is everything you need to bootstrap a brand new rails application inside docker. It's meant to help you develop faster using docker. I haven't tried it in production.

The rails app built is setup to work on mysql. I have also included redis if you are using sidekick.

```
  mkdir app-name
  cd app-name
  git clone https://github.com/jsmootiv/docker-rails .
  rm -rf .git/
  docker-compose run bootstrap
  rm config/database.yml
  cp config/database.template.mysql.yml config/database.yml
  docker-compose run development rake db:create
```

Do your development using:
```
docker-compose up development
```

Do your testing using (assuming that you are using rspec):
```
docker-compose up test
```
