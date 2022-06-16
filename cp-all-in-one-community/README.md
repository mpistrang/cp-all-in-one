![image](../images/confluent-logo-300-2.png)
  
# Documentation

You can find the documentation and instructions for this repo at [https://docs.confluent.io/platform/current/tutorials/build-your-own-demos.html](https://docs.confluent.io/platform/current/tutorials/build-your-own-demos.html?utm_source=github&utm_medium=demo&utm_campaign=ch.examples_type.community_content.cp-all-in-one)


# ksqldb-server Basic Auth Example

To enable basic auth for ksqldb-sever, run:

- `cd cp-all-in-one-community`
- `docker-compose -f docker-compose.yml -f docker-compose.ksqldb-server-basic-auth.yml up -d`

Test basic auth via the curls below:

- `curl -u "my_user:my_password" localhost:8088/v1/metadata`
- `curl -u "my_user:my_password" localhost:8088/healthcheck`

But why does skip.paths not work for the healthcheck?

- `curl localhost:8088/healthcheck`