# simple-ansible-ntp

This should build a simple NTP client-server infrastructure. A node is defined as an ntpserver with
```
ntpserver: true
```
in its `host_vars`, otherwise, it is a client by default. If you want the clients to use a specific server or set of servers, provide a list like this:
```
ntp_servers:
  - ntpserver1
  - ntpserver2
```
otherwise it will just go with the "pool" servers in `roles/ntp/defaults/main.yml`.
