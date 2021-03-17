---
layout: page
title: 'The Microwizard'
---
The Microwizard base system runs inside of a VirtualBox VM. We provision the VM using Vagrant and then use a combination of shell scripts, Ansible playbooks, and custom code to smooth over the experience. Developers must be running a modern Linux distribution or Mac OS X (we’ve tested on Fedora 22 and OS 10.10 Yosemite) and should have the following software installed before trying to use Datawire Microwizard:


| Software    | Version    | Instructions |
| ----------- | ---------- | ------------ |
| Ansible     | &gt;=1.9.4 | `sudo pip install ansible` or see the official [install](http://docs.ansible.com/ansible/intro_installation.html) instructions |
| Vagrant     | &gt;=1.7.4 | [Install instructions](https://docs.vagrantup.com/v2/installation/index.html) |
| Virtual Box | &gt;= 5.0  |[Install instructions](https://www.virtualbox.org/wiki/Downloads) |

### To get started, do the following:

    <script src="https://d3js.org/d3.v5.min.js"></script>
   