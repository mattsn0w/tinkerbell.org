---
title: "Troubleshooting"
draft: false
geekdocDescription: "Troubleshooting common issues when running Tinkerbell."
---

Troubleshooting common issues when running Tinkerbell.


## Issues Encountered
* Kube-vip IP binds to wrong network interface. The ethernet interface needs to have an active link to in order for Kube-vip ARP mode to work correctly.
* Load balancer IP assigned to Traefik Service instead of `tink-stack` Service. K3s needs to be started with traefik disabled. This can be fixed by modifying the `ExecStart` line of `/etc/systemd/system/k3s.service` to include `server --disable=servicelb,traefik,metrics-server`. 
* 
