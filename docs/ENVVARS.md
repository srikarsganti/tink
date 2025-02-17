# Environment Variables

The follow describes environment variables available to be set when running Tink Server, Tink CLI, or Tink Worker.

| Name                                              | Type   | Service(s) | Description                                                                                                                                   |
| ------------------------------------------------- | ------ | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `CAPTURE_ACTION_LOGS=`                            | bool   | worker     | capture action container output as part of worker logs                                                                                        |
| `CERTS_DIR=/certs`                                | string | server     | a directory which contains the `bundle.pem` and `server-key.pem` files, for use when running Tink with TLS                                    |
| `DOCKER_REGISTRY=`                                | string | worker     | the docker registry to use for pulling images                                                                                                 |
| `EVENTS_TTL=60`                                   | string | server     | purges the events in the events table that have passed this TTL in minutes                                                                    |
| `FACILITY=onprem`                                 | string | clients    | location for which the Tink server serves, deprecated in server                                                                               |
| `GRPC_AUTHORITY=127.0.0.1:42113`                  | string | server     | url of the Tink gRPC server                                                                                                                   |
| `HTTP_AUTHORITY=127.0.0.1:42114`                  | string | server     | url of the Tink HTTP server                                                                                                                   |
| `ID=`                                             | string | worker     | the id of the workflow to be executed                                                                                                         |
| `MAX_FILE_SIZE=`                                  | int    | worker     | the maximum size in bytes for the Tink worker data file                                                                                       |
| `MAX_RETRIES=`                                    | int    | worker     | the maximum number of retries for setting up connections and sending status reports to Tink Server                                            |
| `MAX_WORKFLOW_DATA_VERSIONS=`                     | int    | server     | maximum number of workflow data versions to be kept in database                                                                               |
| `ONLY_MIGRATION=true`                             | bool   | server     | if set to true, only POSTGRES migrations are executed                                                                                         |
| `PGDATABASE=tinkerbell`                           | string | server     | same as `POSTGRES_DATABASE`, deprecated in server                                                                                             |
| `PGPASSWORD=tink`                                 | string | server     | same as `POSTGRES_PASSWORD`, deprecated in server                                                                                             |
| `PGSSLMODE=disable`                               | string | server     | same as `POSTGRES_SSLMODE`, deprecated in server                                                                                              |
| `PGUSER=tink`                                     | string | server     | same as `POSTGRES_USER`, deprecated in server                                                                                                 |
| `POSTGRES_DATABASE=tinkerbell`                    | string | server     | name of the PostgreSQL database for use in the Tink server                                                                                    |
| `POSTGRES_PASSWORD=tink`                          | string | server     | PostgreSQL password for connecting to the DB                                                                                                  |
| `POSTGRES_SSLMODE=disable`                        | string | server     | sets the PostgreSQL SSL priority [docs](https://www.postgresql.org/docs/10/libpq-connect.html#LIBPQ-CONNECT-SSLMODE)                          |
| `POSTGRES_USER=tink`                              | string | server     | PostgreSQL username for connecting to the DB                                                                                                  |
| `REGISTRY_PASSWORD=`                              | string | worker     | the password for the docker registry                                                                                                          |
| `REGISTRY_USERNAME=`                              | string | worker     | the username for the docker registry                                                                                                          |
| `RETRY_INTERVAL=`                                 | int    | worker     | the interval in seconds between retries for setting up connections to, querying for workflows from, and sending status reports to Tink Server |
| `TINK_CLI_VERSION="0.0.0"`                        | string | cli        | if set to `0.0.0`, the old get command is used                                                                                                |
| `TINKERBELL_CERTS_DIR=/certs`                     | string | server     | same as `CERTS_DIR`, deprecated in server                                                                                                     |
| `TINKERBELL_CERT_URL=http://127.0.0.1:42114/cert` | string | clients    | url from which to get a TLS certificate, needed when Tink Server's TLS cert is signed by an unknown certificate authority, ie self-signed     |
| `TINKERBELL_GRPC_AUTHORITY=127.0.0.1:42113`       | string | all        | same as `GRPC_AUTHORITY`, deprecated in server                                                                                                |
| `TINKERBELL_HTTP_AUTHORITY=127.0.0.1:42114`       | string | server     | same as `HTTP_AUTHORITY`, deprecated in server                                                                                                |
| `TINKERBELL_TLS="true"`                           | string | all        | configures grpc service or client connections for tls vs plaintext                                                                            |
