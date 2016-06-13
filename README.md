# Ansible Role: Deploy-file

[![Build Status](https://travis-ci.org/AttestationLegale/ansible-role-deploy-file.svg?branch=master)](https://travis-ci.org/AttestationLegale/ansible-role-deploy-file) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-deploy-file-blue.svg)](https://galaxy.ansible.com/AttestationLegale/deploy-file/)

Deploy files from various location and different protocols.

## Requirements

None

## Role Variables

For a complete list of variables, see `default/main.yml`.

    df_entries: []
    df_group_entries: []
    df_host_entries: []

## Dependencies

None

## Example Playbook

```yaml
---
  - hosts: all
    roles:
      - deploy-file
    vars:
      df_entries:
        - type: get_url
          url: "https://www.google.fr/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png"
          dest: "/tmp/google_logo.png"
          mode: "600"

```

Supported types are `get_url` for http / https / ftp and `scp`.

## License

MIT / BSD

## Author Information

This role was created in 2016 by [ALG](https://www.attestationlegale.fr)
