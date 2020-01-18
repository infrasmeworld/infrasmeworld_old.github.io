---
title: "Ansible Notes - become"
date: 2019-12-30
tags: [ansible, devops, automation]
header:
  image: "/images/cloud.png"
excerpt: "ansible, devops, automation"
---

## Become:

Become is used for privilege escalation to execute tasks with root privileges or as another user. If set to "yes", activates privilege escalation. 

Example:

```
- name: Ensure the httpd service is running
  service:
    name: httpd
    state: started
  become: yes
```