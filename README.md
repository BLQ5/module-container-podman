# StackHead: Podman module

StackHead module for using [Podman](https://podman.io) as container provider.

## Installation

Install it via `ansible-galaxy`:

```
ansible-galaxy install getstackhead.stackhead_container_podman
```

In order to use Nginx with [StackHead](https://get.stackhead.io), set `stackhead__container` it in your inventory file:

```yaml
# inventory for integration test
---
all:
  vars:
    # Use Nginx as webserver
    stackhead__container: getstackhead.stackhead_container_podman
  hosts:
    myserver:
      ansible_host: 123.456.789 # ...
      stackhead:
        applications:
          # ...
```
