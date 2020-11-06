## nfs-client

[![Build Status](https://travis-ci.org/Oefenweb/ansible-nfs-client.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-nfs-client)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nfs--client-blue.svg)](https://galaxy.ansible.com/Oefenweb/nfs-client/)

Set up NFS in Debian-like systems (client side)

#### Requirements

None

#### Variables

* `nfs_client_mounts`: [default: `[]`]: Shares to mount
* `nfs_client_mounts.{n}.src`: [required]: The remote path to the share (e.g. `192.168.1.10:/home`)
* `nfs_client_mounts.{n}.path`: [required]: The local path where the share should be mounted (e.g. `/home`)
* `nfs_client_mounts.{n}.state`: [default: `'mounted'`]: State
* `nfs_client_mounts.{n}.fstype`: [default: `'nfs'`]: Filesystem type (e.g. `nfs4`)
* `nfs_client_mounts.{n}.opts`: [optional]: Mount options, see `fstab(5)`
* `nfs_client_mounts.{n}.dump`: [optional]: Dump, see `fstab(5)`
* `nfs_client_mounts.{n}.passno`: [optional]: Passno, see `fstab(5)`

## Dependencies

None

## Recommended

* `ansible-nfs-server` ([see](https://github.com/Oefenweb/ansible-nfs-server))

#### Example

```yaml
---
- hosts: all
  roles:
    - nfs-client
  vars:
    nfs_client_mounts:
      - src: 192.168.1.10:/home
        path: /home
 ``

#### License

MIT

#### Author Information

* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-nfs-client/issues)!
