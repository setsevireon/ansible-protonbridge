ProtonMail Bridge
=========

This role configures ProtonMail Bridge to run as a SystemD service,
using pass and GnuPG to store keys.

**WARNING**: There is a high security risk in using the approach in this role.
First, you will need to provide your password as a role variable. Second, to
run protonmail-bridge non-interactive, it is needed to generate a passwordless
GPG key. I am open to suggestions on safer strategies.

Requirements
------------

- Debian 10+
- A paid ProtonMail account

Role Variables
--------------

Mandatory variables, your ProtonMail credentials:

	protonmail_username: "alibaba"
	protonmail_password: "opensesame"

For internal variables see `vars/main.yml`.


Example Playbook
----------------

```
- hosts: servers
  vars:
    protonmail_username: "alibaba"
    protonmail_password: "opensesame"
  roles:
    - crlsmrx.protonmailbridge
```

License
-------

MIT

Author Information
------------------

[Carlos Marx](https://github.com/crlsmrx)
