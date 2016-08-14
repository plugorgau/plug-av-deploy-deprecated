plug-av-deploy
============

plug-av-deploy is a set of technologies to manage AV equipment and servers.

Core technologies
-----------------
* Ansible

Goals
-----
* (Almost) zero touch service deployment
* Quickly rebuild, deploy and update PLUG AV systems.

Getting Started
===============
Requirements
------------
For a single machine and orchestrator:
* Ubuntu 14.04/16.04 or Debian 8 host machine
* Ansible 2.0+ installed
* sshpass installed

For multiple machines and a single orchestrator:
* Ubuntu 14.04/16.04 or Debian 8 host machine
* Ansible 2.0+ installed
* sshpass installed
* Client machines running Ubuntu 14.04 or Debian 7 and up.

Usage
-----
First-time usage:
* Install Ansible 2.0+ and sshpass on your management workstation

* Clone the plug-av-deploy repositories.

`git clone --recursive https://github.com//magic-glass.git`

`git clone --recursive https://github.com/getglass/magic-glass-secrets.git`

* Follow the instructions for [the magic-glass-secrets repository](https://github.com/getglass/magic-glass-secrets)
* To create the "glass" user according to your preferences (set in group_vars/all), run plug-av-deploy in "bootstrap" mode.

`ansible-playbook site.yml -i inventory --ask-pass --ask-sudo-pass`

* For future runs, simply use this command.

`ansible-playbook site.yml -i inventory` 

* You can also add "--limit=hostgroup" to limit your runs to a specific set of hosts.

Contact Us
==========

IRC
---
You can find us on IRC at #plug on irc.uniirc.com . The IRC channel is a good place to get help or discuss development of plug-av-deploy. However, as plug-av-deploy is not currently in wide distribution, the Gitter channel at the top of this README will be more helpful to you.

Project Details
===============

License
-------
plug-av-deploy is made available under the MIT license and GPLv2 or later. 

See the [LICENSE](LICENSE) file for details.

Branch Info
-----------
* The 'master' branch corresponds to the release actively under development.
* vX.Y.Z tags exist for previous releases.

TODO
----
This is a TODO list specific to the overall project (for tasks that do not belong in a particular module).
* Create a playbook to automatically pull down the latest Ansible on Ubuntu/CentOS?
