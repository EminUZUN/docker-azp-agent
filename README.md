# Docker Azure Pipelines Agent (dsavell/azp-agent)

This repository contains the Dockerfiles & images for the Azure DevOps pipeline agent that runs tasks as part of a build or release pipelines.

Azure Pipelines Agent images are tagged according to the base OS.

## Docker Image Contents

- [Ubuntu 16.04](https://github.com/dsavell/docker-azp-agent/tree/master/ubuntu/1604)
- [Ubuntu 18.04](https://github.com/dsavell/docker-azp-agent/tree/master/ubuntu/1804)

## Usage

Run the container. This will install the latest version of the agent, configure it, and run the agent targeting a pool of a specified Azure DevOps or Azure DevOps Server instance of your choice:

### Ubuntu 16.04

```
docker run \
  -e AZP_URL=<Azure DevOps instance> \
  -e AZP_TOKEN=<PAT token> \
  -e AZP_AGENT_NAME=mydockeragent \
  -e AZP_POOL=mypool \
  -v /var/run/docker.sock:/var/run/docker.sock \
  dsavell/azp-agent:ubuntu-16.04
```

### Ubuntu 18.04

```
docker run \
  -e AZP_URL=<Azure DevOps instance> \
  -e AZP_TOKEN=<PAT token> \
  -e AZP_AGENT_NAME=myagent \
  -e AZP_POOL=mypool \
  -v /var/run/docker.sock:/var/run/docker.sock \
  dsavell/azp-agent:ubuntu-18.04
```
