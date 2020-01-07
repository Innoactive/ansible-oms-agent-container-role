# Role Name

Installs the Microsoft Operations Management Suite Agent as a docker container as described in
https://docs.microsoft.com/en-us/azure/azure-monitor/insights/containers#install-and-configure-linux-container-hosts.

## Installation

To install this role locally, simply run `ansible-galaxy install git+git@github.com:Innoactive/ansible-innoactive-hub-role.git`.

## Requirements

The host this role is applied to needs to be running docker; to meet this requirement, use e.g. [the docker role](https://galaxy.ansible.com/geerlingguy/docker).

## Role Variables

    azure_log_analytics_workspace_id:

The workspace id of the Azure Log Analytics workspace.

    azure_log_analytics_primary_key:

The primary key to authenticate with the Azure Log Analytics workspace.

    oms_hostname:

The hostname that will be stored along with all of the oms metrics.


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        azure_log_analytics_workspace_id: your-azure-log-analytics-workspace-id
        azure_log_analytics_primary_key: your-azure-log-analytics-primary-key
        oms_hostname: hostname-to-associate-with-metrics
      roles:
         - ansible-oms-agent-container-role

## License

Apache 2.0
