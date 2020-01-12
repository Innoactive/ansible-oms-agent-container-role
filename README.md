# Role Name

Installs the Microsoft Operations Management Suite Agent with support for container monitoring. This is effectively a
wrapper around the excellent [svendewindt.omsagentlinux-role](https://github.com/svendewindt/ansible-role-omsagent-linux)
which installs the oms-agent for linux. Since we also want to monitor docker containers though, we need to apply the
workaround stated in the [release notes of the docker-based oms-agent](https://github.com/Microsoft/OMS-docker/blob/master/ReleaseNote.md#due-to-the-backend-changes-for-container-monitoring-with-oms-agent-for-linux-and-it-is-a-fresh-install-you-will-need-to-run-this-workaround).

## Installation

To install this role locally, simply run `ansible-galaxy install git+git@github.com:Innoactive/ansible-innoactive-hub-role.git`.

## Requirements

The host this role is applied to needs to be running docker; to meet this requirement, use e.g. [the docker role](https://galaxy.ansible.com/geerlingguy/docker).

## Role Variables

Since this role is nothing but a thin wrapper around [svendewindt.omsagentlinux](https://github.com/svendewindt/ansible-role-omsagent-linux)
please refer to the [docs there with respect to the available / required variables.](https://github.com/svendewindt/ansible-role-omsagent-linux#role-variables)

## Example Playbook

See [svendewindt/ansible-oms-agent-role#example-playbook](https://github.com/svendewindt/ansible-role-omsagent-linux#example-playbook).

## License

Apache 2.0
