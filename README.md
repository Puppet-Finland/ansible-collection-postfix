# Ansible Collection - puppeteers.postfix

Ansible collection for configuring postfix.

# Roles

## puppeteers.postfix.relayhost

This role sets up postfix as a relayhost. The main use case is to provide SMTP
forwarding services for servers in private networks where direct egress to the
Internet is missing completely, or is only partial (e.g. IPv6 only). Postfix
sends emails using a real email account on an upstream (e.g. Google) email
server.

Parameters:
- *puppeteers_postfix_relayhost_relayhost:* the IP address or hostname of the upstream SMTP server (e.g. Google SMTP server)
- *puppeteers_postfix_relayhost_relayhost_port:* the port for the upstream SMTP server
- *puppeteers_postfix_relayhost_smtp_username:* upstream SMTP server username
- *puppeteers_postfix_relayhost_smtp_password:* upstream SMTP server user password
- *puppeteers_postfix_relayhost_mynetworks:* a network block from which to allow SMTP connections to postfix

# License

[BSD-2-Clause](LICENSE)
