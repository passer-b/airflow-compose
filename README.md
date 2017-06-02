# airflow-compose

### usage

``` bash
docker-compose up -d
```

### composition

name      | description
:---      | :---
webserver | Web UI
scheduler | task scheduler
postgres  | meta data store
redis     | celery backend
