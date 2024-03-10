---
tags:
  - linux
  - ssh
---
# How to force the SSH client to use only provided identity

When we connect to a remote SSH server, the ssh-agent may try to authenticate using many different identities.
Sometimes this behavior may cause issues, so we may want to tell the SSH client to use only the identity we configured or provided for that specific connection. 

To this purpose we can use the `IdentitiesOnly` option.

> `IdentitiesOnly`
> Specifies that ssh(1) should only use the configured authentication identity and certificate files (either the default files, or those explicitly configured in the ssh_config files or passed on the ssh(1) command-line), even if ssh-agent(1) or a PKCS11Provider or SecurityKeyProvider offers more identities.  The argument to this keyword must be yes or no (the default).  This option is intended for situations where ssh-agent offers many different identities.

```shell
ssh -o IdentitiesOnly=yes -i identity.key user@host
```

To persist this behavior, modify the `/etc/ssh/ssh_config` file by adding this line:

```conf
IdentitiesOnly yes
```
