Home Assistant for private/internal use in (Bootable) Containers
================================================================

```
$ podman run -d --name homeassistant --hostname ${HOSTNAME}-homeassistant \
    --net=nroute-switch --ip 10.0.21.90 \
    --cap-add=NET_ADMIN --cap-add=NET_RAW --device=/dev/net/tun \
    ghcr.io/gbraad-homelab/private-homeassistant:latest
```