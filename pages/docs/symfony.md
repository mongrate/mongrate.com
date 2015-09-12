---
layout: page
permalink: /docs/symfony.html
title: How to use Mongrate with Symfony
content_title: Symfony integration
excerpt: In addition to the standalone installation, there is a Symfony bundle.
---

In addition to the [standalone installation](/docs/installation), there is a Symfony bundle, which
lets you use the Mongrate commands by running your `app/console` (`bin/console` in Symfony3).

Installation
------------

In your Symfony application directory, run:

`composer require amyboyd/mongrate-bundle`

Set your configuration in your application's `config.yml`:

<pre>
mongrate:
    mongodb_server: 'mongodb://localhost:27017'
    mongodb_db: my_database
    migrations_directory: "%kernel.root_dir%/../migrations"
</pre>

As always, you can use settings from `parameters.yml` with `%...%`. For example:

<pre>
mongrate:
    mongodb_server: %mongodb_server%
    mongodb_db: %mongodb_db%_prod
</pre>

Commands
--------

The only difference to using the standalone installation is that instead of running, for example,
`mongrate list-migrations`, when using the bundle you should run
`app/console mongrate:list-migrations`.

See the commands available by running `app/console list mongrate`
