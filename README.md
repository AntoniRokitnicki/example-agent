## Push To Docker Registry Workflow
Workflow builds docker image with name `"${System.env.DOCKER_REGISTRY_URL}/${System.env.DOCKER_ORGANIZATION}/example-agent:@project.version"` and pushes the image
into configured docker registry.

The GitHub secrets in table below needs to be configured:

| Name | Description |
| ---- | ----------- |
| DOCKER_USERNAME | Username for Docker registry authentication. |
| DOCKER_PASSWORD | Docker registry password. |
| DOCKER_ORGANIZATION | Path to the docker image registry, e.g. for image `foo/bar/micronaut:0.1` it is `foo/bar`. |
| DOCKER_REGISTRY_URL | Docker registry url. |
### Examples of configuration
> Specifics on how to configure public cloud docker registries like DockerHub, Google Container Registry (GCR), AWS Container Registry (ECR),
> Oracle Cloud Infrastructure Registry (OCIR) and many more can be found in [docker/login-action](https://github.com/docker/login-action)
> documentation.

#### DockerHub

- `DOCKER_USERNAME` - DockerHub username
- `DOCKER_PASSWORD` - DockerHub password or personal access token
- `DOCKER_ORGANIZATION` - DockerHub organization or the username in case of personal registry
- `DOCKER_REGISTRY_URL` - No need to configure for DockerHub

> See [docker/login-action for GCR](https://github.com/docker/login-action#dockerhub)

#### Google Container Registry (GCR)
Create service account with permission to edit GCR or use predefined Storage Admin role.

- `DOCKER_USERNAME` - set exactly to `_json_key`
- `DOCKER_PASSWORD` - content of the service account json key file
- `DOCKER_ORGANIZATION` - `<project-id>`
- `DOCKER_REGISTRY_URL` - `gcr.io`

> See [docker/login-action for GCR](https://github.com/docker/login-action#google-container-registry-gcr)

#### AWS Elastic Container Registry (ECR)
Create IAM user with permission to push to ECR (or use AmazonEC2ContainerRegistryFullAccess role).

- DOCKER_USERNAME - access key ID
- DOCKER_PASSWORD - secret access key
- DOCKER_ORGANIZATION - no need to set
- DOCKER_REGISTRY_URL - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for ECR](https://github.com/docker/login-action#aws-elastic-container-registry-ecr)

#### Oracle Infrastructure Cloud Registry (OCIR)
[Create auth token](https://www.oracle.com/webfolder/technetwork/tutorials/obe/oci/registry/index.html#GetanAuthToken) for authentication.

- DOCKER_USERNAME - username in format `<tenancy>/<username>`
- DOCKER_PASSWORD - account auth token
- DOCKER_ORGANIZATION - `<tenancy>/<registry>`
- DOCKER_REGISTRY_URL - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for OCIR](https://github.com/docker/login-action#oci-oracle-cloud-infrastructure-registry-ocir)
## Push GraalVM Native Image To Docker Registry Workflow
Workflow builds docker image with name `"${System.env.DOCKER_REGISTRY_URL}/${System.env.DOCKER_ORGANIZATION}/example-agent:@project.version"` and pushes the image
into configured docker registry.

The GitHub secrets in table below needs to be configured:

| Name | Description |
| ---- | ----------- |
| DOCKER_USERNAME | Username for Docker registry authentication. |
| DOCKER_PASSWORD | Docker registry password. |
| DOCKER_ORGANIZATION | Path to the docker image registry, e.g. for image `foo/bar/micronaut:0.1` it is `foo/bar`. |
| DOCKER_REGISTRY_URL | Docker registry url. |
### Examples of configuration
> Specifics on how to configure public cloud docker registries like DockerHub, Google Container Registry (GCR), AWS Container Registry (ECR),
> Oracle Cloud Infrastructure Registry (OCIR) and many more can be found in [docker/login-action](https://github.com/docker/login-action)
> documentation.

#### DockerHub

- `DOCKER_USERNAME` - DockerHub username
- `DOCKER_PASSWORD` - DockerHub password or personal access token
- `DOCKER_ORGANIZATION` - DockerHub organization or the username in case of personal registry
- `DOCKER_REGISTRY_URL` - No need to configure for DockerHub

> See [docker/login-action for GCR](https://github.com/docker/login-action#dockerhub)

#### Google Container Registry (GCR)
Create service account with permission to edit GCR or use predefined Storage Admin role.

- `DOCKER_USERNAME` - set exactly to `_json_key`
- `DOCKER_PASSWORD` - content of the service account json key file
- `DOCKER_ORGANIZATION` - `<project-id>`
- `DOCKER_REGISTRY_URL` - `gcr.io`

> See [docker/login-action for GCR](https://github.com/docker/login-action#google-container-registry-gcr)

#### AWS Elastic Container Registry (ECR)
Create IAM user with permission to push to ECR (or use AmazonEC2ContainerRegistryFullAccess role).

- DOCKER_USERNAME - access key ID
- DOCKER_PASSWORD - secret access key
- DOCKER_ORGANIZATION - no need to set
- DOCKER_REGISTRY_URL - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for ECR](https://github.com/docker/login-action#aws-elastic-container-registry-ecr)

#### Oracle Infrastructure Cloud Registry (OCIR)
[Create auth token](https://www.oracle.com/webfolder/technetwork/tutorials/obe/oci/registry/index.html#GetanAuthToken) for authentication.

- DOCKER_USERNAME - username in format `<tenancy>/<username>`
- DOCKER_PASSWORD - account auth token
- DOCKER_ORGANIZATION - `<tenancy>/<registry>`
- DOCKER_REGISTRY_URL - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for OCIR](https://github.com/docker/login-action#oci-oracle-cloud-infrastructure-registry-ocir)
## Feature kafka-streams documentation

- [Micronaut Kafka Streams documentation](https://micronaut-projects.github.io/micronaut-kafka/latest/guide/index.html#kafkaStream)

## Feature jackson-xml documentation

- [Micronaut Jackson XML serialization/deserialization documentation](https://micronaut-projects.github.io/micronaut-jackson-xml/latest/guide/index.html)

- [https://github.com/FasterXML/jackson-dataformat-xml](https://github.com/FasterXML/jackson-dataformat-xml)

## Feature jdbc-hikari documentation

- [Micronaut Hikari JDBC Connection Pool documentation](https://micronaut-projects.github.io/micronaut-sql/latest/guide/index.html#jdbc)

## Feature github-workflow-docker-registry documentation

- [https://docs.github.com/en/free-pro-team@latest/actions](https://docs.github.com/en/free-pro-team@latest/actions)

## Feature spring documentation

- [Micronaut Spring Framework Annotations documentation](https://micronaut-projects.github.io/micronaut-spring/latest/guide/index.html)

## Feature hibernate-validator documentation

- [Micronaut Hibernate Validator documentation](https://micronaut-projects.github.io/micronaut-hibernate-validator/latest/guide/index.html)

## Feature liquibase documentation

- [Micronaut Liquibase Database Migration documentation](https://micronaut-projects.github.io/micronaut-liquibase/latest/guide/index.html)

- [https://www.liquibase.org/](https://www.liquibase.org/)

## Feature hibernate-jpa documentation

- [Micronaut Hibernate JPA documentation](https://micronaut-projects.github.io/micronaut-sql/latest/guide/index.html#hibernate)

## Feature kafka documentation

- [Micronaut Kafka Messaging documentation](https://micronaut-projects.github.io/micronaut-kafka/latest/guide/index.html)

## Feature github-workflow-graal-docker-registry documentation

- [https://docs.github.com/en/free-pro-team@latest/actions](https://docs.github.com/en/free-pro-team@latest/actions)

## Feature testcontainers documentation

- [https://www.testcontainers.org/](https://www.testcontainers.org/)

