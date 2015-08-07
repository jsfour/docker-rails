# Rails Docker Install

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
