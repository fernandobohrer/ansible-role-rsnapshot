# Ansible Role: rsnapshot

An Ansible role that deploys and configures [rsnapshot][01] on Linux boxes.

## 🚀 Motivation

From rsnapshot's [site][01]:

_rsnapshot is a filesystem snapshot utility based on rsync. rsnapshot makes it easy to make periodic snapshots of local machines, and remote machines over ssh. The code makes extensive use of hard links whenever possible, to greatly reduce the disk space required._

_Files can be restored by the users who own them, without the root user getting involved. There are no tapes to change, so once it's set up, your backups can happen automatically untouched by human hands. And because rsnapshot only keeps a fixed (but configurable) number of snapshots, the amount of disk space used will not continuously grow._

This role deploys and configures [rsnapshot][01] on Linux boxes.

## 📑 Role Variables

Check [defaults/main.yml][02].

## 🧰 Dependencies

None.

## ⚡ Quick start

An example of how integrate this role to an Ansible playbook can be found here:

```yml
---
- name: Deploy rsnapshot
  hosts: all
  become: true
  gather_facts: true
  roles:
    - fernandobohrer.rsnapshot
```

## ⚙️ Compatibility

This role was tested on and is confirmed to work with the following Linux distributions:

- `Debian 13`
- `Ubuntu 24.04`

Details can be found in the [Molecule][03] scenarios available in the `molecule` folder.

## ⚠️ Warning

This Ansible role was tested on the above mentioned Linux distributions considering their default configuration. Your environment might have a different configuration or requirements which might conflict with the options that this role uses.

With the above in mind, it is **imperative** that you familiarize yourself with what this role does and test it on non-production machines **before** applying it to machines in a production environment.

## 📝 License

This project is licensed under the terms of the [MIT license][04].

[01]: https://rsnapshot.org/
[02]: defaults/main.yml
[03]: https://github.com/fernandobohrer/ansible-molecule-scenarios
[04]: /LICENSE
