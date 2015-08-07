# Rails Docker Install

```
  docker-compose run bootstrap
  rm config/database.yml
  cp config/database.template.mysql.yml config/database.yml
  docker-compose run development rake db:create
```
