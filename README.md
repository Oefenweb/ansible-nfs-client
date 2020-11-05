## nfs-client

[![Build Status](https://travis-ci.org/Oefenweb/ansible-nfs-client.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-nfs-client)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nfs--client-blue.svg)](https://galaxy.ansible.com/Oefenweb/nfs-client/)

Set up NFS in Debian-like systems (client side)

#### Requirements

None

#### Variables

* `nfs_client_exports`: [see: `defaults/main.yml`]: List of lines to be added to `/etc/exports`

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - nfs-client
 ``

#### License

MIT

#### Author Information

* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-nfs-client/issues)!
