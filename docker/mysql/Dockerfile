ARG mysql_version

FROM mysql:${mysql_version}

COPY entrypoint/* docker-entrypoint-initdb.d/
