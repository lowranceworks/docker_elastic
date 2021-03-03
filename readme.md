# Elasticsearch and Kibana on Docker

## Getting started
**References** \
. \
. \
https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-docker.html
https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docker.html#docker-cli-run-dev-mode  


**Install and configure Docker** \
Install Docker \
.
```
sudo systemctl enable docker && \
sudo gpasswd -a $USER docker && \
sudo su $USER 
```


**Install Docker-Compose** \
Install Docker-Compose 
```

```

**Pulling the Docker image** \
Obtaining Elasticsearch for Docker is as simple as issuing a docker pull command against the Elastic Docker registry.
```
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.5.2
```

**Starting a multi-node cluster with Docker Compose** \
- docker-compose.yml

**Disclaimer** \
Please note that this configuration exposes port 9200 on all network interfaces, and given how Docker manipulates iptables on Linux, this means that your Elasticsearch cluster is publically accessible, potentially ignoring any firewall settings. If you don’t want to expose port 9200 and instead use a reverse proxy, replace 9200:9200 with 127.0.0.1:9200:9200 in the docker-compose.yml file. Elasticsearch will then only be accessible from the host machine itself.

## Troubleshooting

**Error:** \
docker.errors.DockerException: Error while fetching server API version: ('Connection aborted.', PermissionError(13, 'Permission denied'))** 

**Resolution:** \
Grant user rights to docker, sign out and sign back in 
```
sudo gpasswd -a $USER docker && sudo su $USER
```

**Error:** \
Failed to execute script docker-compose

**Resolution** 
```
sudo systemctl restart docker 
```

**Error:** \
.

**Resolution:**
```
```

**Error:** \
.

**Resolution:**
```
```