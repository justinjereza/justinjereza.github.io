---
layout: basic
title: Foreman notes
---
Foreman
=======

Installation
------------
```sh
foreman-installer --puppet-server-dynamic-environments=true --puppet-server-git-repo=true
```

Configuration
-------------
- Add `/etc/puppet/modules` to `modulepath` in `/etc/puppet/puppet.conf` so that each environment has access to installed modules. `puppet module install --environment=foo my_module` is broken in 2.7.

Puppet Modules
--------------
- puppetlabs-apt
- trlinkin-nsswitch
- saz-sudo
