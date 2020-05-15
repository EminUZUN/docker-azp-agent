# Docker Azure Pipelines Agent (dsavell/azp-agent)

This repository contains the Dockerfiles & images for the Azure DevOps pipeline agent that runs tasks as part of a build or release pipelines.

Azure Pipelines Agent images are tagged according to the base OS.

## Docker Image Contents

- [Ubuntu 18.04](https://github.com/dsavell/docker-azp-agent/tree/master/ubuntu/1804)
- [Ubuntu 20.04](https://github.com/dsavell/docker-azp-agent/tree/master/ubuntu/2004)

## Usage

Run the container. This will install the latest version of the agent, configure it, and run the agent targeting a pool of a specified Azure DevOps or Azure DevOps Server instance of your choice:

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

### Ubuntu 20.04

```
docker run \
  -e AZP_URL=<Azure DevOps instance> \
  -e AZP_TOKEN=<PAT token> \
  -e AZP_AGENT_NAME=myagent \
  -e AZP_POOL=mypool \
  -v /var/run/docker.sock:/var/run/docker.sock \
  dsavell/azp-agent:ubuntu-20.04
```
