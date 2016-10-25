pack-coreos-ssh
===============

Configuration pack for CoreOS hosts based on SSH checks

Based on https://github.com/naparuba/check-linux-by-ssh and https://github.com/naparuba/pack-linux-ssh

For Authorized_keys, you have to edit the /etc/shinken/resource.d/ssh.cfg file if need:

```
$SSH_KEY$=~/.ssh/id_rsa
$SSH_KEY_PASSPHRASE$=''
$SSH_USER$=shinken
$SSH_PORT$=22$
```

NOTES
=====

The check-linux-ssh scripts should be at least in version
086e5bbc7e5435a4980c60532c9fb4fc57ebe40f (git commit, PR 53) in order to be
allow to use the '-e' option on the check_ro_filesystem_by_ssh check.
