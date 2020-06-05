# Ansible Role: Longview

Installs and configures [Linode Longview service](https://www.linode.com/docs/platform/longview/what-is-longview) for host monitoring.

## Requirements

Debian-based only.  Tested on Ubuntu 20.04.

## Role Variables

You must set your Longview API key:

    longview_api_key: "your-api-key"

Copy the API key from the Installation tab of your Longview client’s detailed view in the Linode Cloud Manager.

## Example Playbook

    - hosts: server
      vars_files:
        - vars/main.yml
      roles:
        - role: ansible-longview

*Inside `vars/main.yml`*:

    longview_api_key: "your-api-key"

## License

MIT