---
layout: page
permalink: /docs/installation.html
title: How to install Mongrate
content_title: Installation
---

Requirements
============

* [PHP >= 5.5.0](https://secure.php.net/manual/en/install.php) (lower versions are untested)
* [PHP MongoDB extension](https://secure.php.net/manual/en/mongo.installation.php)

Standalone install
==================

This method of installing requires just PHP to be installed. It is the simplest method and a good
way to get started. It will work for projects of any size.

<pre>
sudo wget mongrate.com/download -O /usr/bin/mongrate
sudo chmod +x /usr/bin/mongrate
sudo wget mongrate.com/sample-config.yml -O /etc/mongrate.yml
</pre>

Now verify the install has been successful by running `mongrate`. You should see a list of available
commands, and no error messages.

If successful, you can now configure mongrate in `/etc/mongrate.yml`.

Configuration
=============

By default, you should configure Mongrate in `/etc/mongrate.yml`

| Parameter             | Required? | Description  |
| -------------         |:---------:| :------------|
| mongodb_server        | yes       | URI for your MongoDB server. |
| mongodb_db            | yes       | Database name. |
| migrations_directory  | yes       | The directory where your migration files are to be kept. |

Symfony integration
===================

In addition to the standalone installation, there is a Symfony bundle, which lets you use the
Mongrate commands by running your `app/console` (`bin/console` in Symfony3).

For information, see [this page](/docs/symfony).

Puppet
======

Installing via Puppet couldn't be easier.

For information, see [this page](/docs/puppet).
