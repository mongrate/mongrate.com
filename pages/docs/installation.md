---
layout: page
permalink: /docs/installation.html
title: How to install Mongrate
content_title: Installation
---

Requirements
============

* PHP >= 5.4.0
* PHP MongoDB extension

Standalone install
==================

This method of installing requires just PHP to be installed. It is the simplest method and a good
way to get started. It will work for projects of any size.

<pre>
sudo wget mongrate.com/download -O /usr/bin/mongrate
sudo chmod +x /usr/bin/mongrate
sudo wget mongrate.com/sample-config.yml -O /etc/mongrate.yml
</pre>

Now verify the install has been successful by running `mongrate`.

If successful, you can now configure mongrate in `/etc/mongrate.yml`.

Symfony integration
===================

In addition to the standalone installation, there is a Symfony bundle, which lets you use the
Mongrate commands by running your `app/console` (`bin/console` in Symfony3).

For information, see [this page](/docs/symfony).
