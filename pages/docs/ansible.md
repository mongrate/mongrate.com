---
layout: page
permalink: /docs/ansible.html
title: How to install Mongrate via Ansible
content_title: Ansible installation
excerpt: If you use Ansible to manage your servers, installing Mongrate via Ansible is easy.
---

If you use [Ansible](https://www.ansible.com/) to manage your servers, installing Mongrate via Ansible
is easy:

<pre>
- name: Install Mongrate
  get_url: url=http://mongrate.amyboyd.co.uk/download?ansible dest=/usr/bin/mongrate mode=0555 force=no
</pre>

Configuring `/etc/mongrate.yml` is up to you, but you can download the sample file easily too:

<pre>
- name: Copy default Mongrate configuration
  get_url: url=http://mongrate.amyboyd.co.uk/sample-config.yml?ansible dest=/etc/mongrate.yml force=no
</pre>
