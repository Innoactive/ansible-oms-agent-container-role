# Role Name

Installs the Microsoft Operations Management Suite Agent with support for container monitoring. This is largely based on
the excellent [svendewindt.omsagentlinux-role](https://github.com/svendewindt/ansible-role-omsagent-linux)
which installs the oms-agent for linux. Since we also want to monitor docker containers though, we need to apply the
workaround stated in the [release notes of the docker-based oms-agent](https://github.com/Microsoft/OMS-docker/blob/master/ReleaseNote.md#due-to-the-backend-changes-for-container-monitoring-with-oms-agent-for-linux-and-it-is-a-fresh-install-you-will-need-to-run-this-workaround).

## Installation

To install this role locally, simply run `ansible-galaxy install git+git@github.com:Innoactive/ansible-innoactive-hub-role.git`.

## Requirements

The host this role is applied to needs to be running docker (otherwise container monitoring will not work); to meet this
requirement, use e.g. [the docker role](https://galaxy.ansible.com/geerlingguy/docker).

## Role Variables

The variables have been partially taken from [svendewindt.omsagentlinux](https://github.com/svendewindt/ansible-role-omsagent-linux):

| Variable                  | Default | Comments (type)                                                                |
| ---                       | ---     | ---                                                                            |
| `workspace_id`            | -       | Required. The workspace ID                                                     |
| `workspace_key`           | -       | Required. The workspace Key                                                    |

## Example Playbook

See [svendewindt/ansible-oms-agent-role#example-playbook](https://github.com/svendewindt/ansible-role-omsagent-linux#example-playbook).

## License

Apache 2.0
