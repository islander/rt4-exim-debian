Request Tracker 4
=========

Role for installing Request-Tracker 4 on Debian 9 (stretch). And config for
Exim4 integration with `rt-mailgate`.

Powered by [molecule](https://molecule.readthedocs.io/en/latest/).

Requirements
------------

[Vagrant](https://www.vagrantup.com) - for `molecule` (testing).

Role Variables
--------------

 * `aptproxy`: APT proxy
 * `mailname`: Mailname for Exim4
 * `random_passwd`: Randomly generated password. Need for MySQL exim user.

Dependencies
------------

__No dependencies for now__

Example Playbook
----------------

    - hosts: servers
      become: yes
      roles:
         - { role: rt4-exim4-debian, aptproxy: "192.0.2.254" }

License
-------

BSD

Author Information
------------------

 * [kiba](https://github.com/islander)

References
----------
 * https://rt-wiki.bestpractical.com/wiki/ConfigEximFromRTDB
 * https://github.com/annaken/annaken.github.io/blob/421cf769af188592afed413f626295d6c76abda8/_posts/2013-08-14-setting-up-rt4.md
 * https://wikitech.wikimedia.org/wiki/RT
 * https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=238345
 * https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=229052
 * https://forum.bestpractical.com/t/problem-to-integrate-exim4-with-request-tracker-4-0/30306/6
