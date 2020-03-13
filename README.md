## About
This project provides [Portainer](https://www.portainer.io/) container templates for [Zeebe](https://zeebe.io/).

These templates are intended to quickly spin up a Zeebe node or cluster and take it for a test drive. They are not intended or recommended for production.

### Templates
* Zeebe Standalone Broker (latest, 0.22.2) - Zeebe workflow engine with a single broker
* Zeebe Cluster S (0.22.2) - Small Zeebe workflow engine cluster with three brokers and a gateway

### Broken templates (a.k.a work in progress)
* Zeebe Broker + Operate - Zeebe workflow engine with a broker and Operate frontend

### Usage
Assuming you have Docker and Portainer set up and running:

1. Open Portainer web console
1. Click on _Settings_
1. Toggle _Use external templates_ to _On_
1. Copy this URL into the input field below the toggle: `https://pihme.github.io/zeebe-portainer-templates/templates.json`
1. Click _Save Settings_
1. Click on _Home_ and select the Docker host on which you want to deploy Zeebe
1. Click on _App Templates_
1. Choose the template you want to use
1. Click on _Deploy the Container_ or _Deploy the stack_
1. Wait until the container(s) are running

#### Optional Step
Before deploying the template, you can select _Show advanced options_. This allows you, among others, to specify the port mapping.

#### Restoring default templates
1. Open Portainer web console
1. Click on _Settings_
1. Toggle _Use external templates_ to _Off_
1. Click _Save Settings_

### Next steps
Now that you have Zeebe running in Docker, you can direct a [client]([https://docs.zeebe.io/clients/index.html) at it and start experimenting.
All templates are configured to expose port `26500` for clients to connect to.

Later, if you want to gain more control over how Zeebe is deployed, you might want to look at:
* [zeebe-docker-compose](https://github.com/zeebe-io/zeebe-docker-compose): Which contains customizable docker compose files
* [zeeb-helm](https://helm.zeebe.io/): Which contains helm charts to deploy Zeebe to Kubernetes

