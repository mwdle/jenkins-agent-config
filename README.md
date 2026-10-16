# Jenkins Agent Configuration

A rootless Podman Quadlet deployment for permanent Jenkins agents.

The container image is built and published by [jenkins-agent](https://github.com/mwdle/jenkins-agent).

## Jenkins configuration

The Jenkins node name is derived from the deployment host's systemd `%H` hostname specifier. Create a matching permanent inbound node in Jenkins before deploying the agent. For example, a host named `lab` requires a Jenkins node named `lab`.

Store the node's secret as a Jenkins Secret text credential with the ID `jenkins-agent-secret`. The deployment pipeline provisions it in the target user's Podman secret store as `jenkins_agent_secret` before installing the Quadlet.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details
