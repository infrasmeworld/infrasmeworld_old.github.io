---
title: "Ansible Notes - shell"
date: 2019-12-30
tags: [Ansible, devops]
header:
  image: "/images/cloud.png"
excerpt: "ansible, devops, automation"
---

The shell module can be used to execute shell commands on target hosts.

Example:

    - name: Backup the current nsswitch config file
      shell: "mv /etc/nsswitch.conf /etc/nsswitch.conf_`date +%F`"



