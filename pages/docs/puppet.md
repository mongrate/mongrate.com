---
layout: page
permalink: /docs/puppet.html
title: How to install Mongrate via Puppet
content_title: Puppet installation
excerpt: If you use Puppet to manage your servers, installing Mongrate via Puppet is easy.
---

If you use [Puppet](https://puppetlabs.com/) to manage your servers, installing Mongrate via Puppet
is easy:

<pre>
exec { 'Download mongrate.phar':
  command => '/usr/bin/wget mongrate.com/download?puppet -O /usr/bin/mongrate',
  creates => '/usr/bin/mongrate',
}

file { '/usr/bin/mongrate':
  ensure  => present,
  mode    => '0555',
  require => Exec['Download mongrate.phar'],
}
</pre>

Configuring `/etc/mongrate.yml` is up to you, but you can download the sample easily too:

<pre>
exec { 'Download mongrate.yml':
  command => '/usr/bin/wget mongrate.com/sample-config.yml?puppet -O /etc/mongrate.yml',
  creates => '/etc/mongrate.yml',
}
</pre>
