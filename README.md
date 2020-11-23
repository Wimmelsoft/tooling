This repository holds the docker configuration
for the following tools suite:
- Jenkins
- Bitbucket with postgreSQL
- Standalone PostgreSQL for generic purposes

Not included with the repository but should be in the filesystem:
- jdk-11.0.9.1+1 or equivalent. Jenkins does not come with jdk-11, and therefore is added to the container. See Dockerfile
- apache-maven-3.6.3 Add the latest Maven version to Jenkins
- data directories for Jenkins (to persist the workspace and configuration)
- data directories for the databases

Before starting the stack:

```
docker volume create bitbucketVolume
```

Then execute the following command:

```
docker stack deploy -c ./tools.yml tools
```

Issue: bitbucket keeps starting up in the setup, and does not persist the configuration

