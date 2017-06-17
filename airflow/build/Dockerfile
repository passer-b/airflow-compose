FROM passant/airflow:latest

RUN apk add --no-cache --virtual .airflow-postgres-builddep \
		alpine-sdk \
	&& apk add --no-cache --virtual .airflow-postgres-rundep \
		postgresql-dev \
	&& pip install --proxy "${http_proxy}" redis \
	&& pip install --proxy "${http_proxy}" airflow[celery,ldap,s3,postgres] \
	&& apk del .airflow-postgres-builddep
