# airflow-compose

### usage

``` bash
cp airflow/data/sirflow.cfg.sample airflow/data/sirflow.cfg
docker-compose up -d postgres redis
docker-compose up -d scheduler
docker-compose up -d webserver
docker-compose up -d worker
open http://localhost:18080
```

### composition

name      | description
:---      | :---
webserver | Web UI
scheduler | task scheduler
worker    | task worker
postgres  | meta data store
redis     | celery backend
