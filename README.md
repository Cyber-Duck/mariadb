# About this Repo

This is a fork of the Docker [official image](https://docs.docker.com/docker-hub/official_repos/) for [mariadb](https://registry.hub.docker.com/_/mariadb/).
See [the official mariadb Docker Hub page](https://registry.hub.docker.com/_/mariadb/) for the original full readme on how to use this Docker image and for information regarding contributing and issues.

## Adding `MYSQL_SECONDARY_DATABASE` environment variable support

Because we always need to have a `test` database created to run our unit tests on a separate (but still related) database, we decided to add a new environment variable to create that optional secondary database upon image startup.
Similar to `MYSQL_DATABASE`, the `MYSQL_USER` created upon image startup will have full rights over this one.
This is very useful for our internal development workflow.

See [our Docker Hub page](https://registry.hub.docker.com/cyberduck/mariadb/) for the full readme updated with our changes.
