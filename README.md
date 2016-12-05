# Ansible Role: Mac App Store CLI (mas)

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-mas.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-mas)

Installs [mas](https://github.com/mas-cli/mas) on macOS, and installs macOS apps from the Mac App Store.

## Requirements

  - Requires `homebrew` already installed.
  - Must be signed into Mac App Store already
    - You can either sign in via GUI, or with `mas signin mas@example.com`

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    mas_installed_app_ids:
      # Xcode (7.0).
      - 497799835

TODO.

    mas_upgrade_all_apps: no

TODO.

## Dependencies

  - `geerlingguy.homebrew`

## Example Playbook

    - hosts: localhost
      vars:
        mas_installed_app_ids:
          # Xcode (7.0).
          - 497799835
      roles:
        - geerlingguy.homebrew

See the [Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook) for an example of this role's usage.

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Jeff Geerling](http://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
