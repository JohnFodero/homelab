# Start Here

## Goals :goal:
* Learn stuff, hands-on, like Kubernetes, GitOps, networking (SSL, VLANs, DNS, DHCP), and routing (hardware, OSS)
* Keep it low(ish) power, with backups and smart server power control
* Have access to VMs for prototyping and development
* Host all of my favorite local apps
* Make it all easily deployable and as "highly available" as possible for a homelab

## Feature Checklist
- [ ] SSO
- [ ] System monitoring
- [ ] GitOps management
- [ ] Power monitoring and management
- [ ] Automated node creation/provisioning
- [ ] Service tunnel
- [ ] Distributed storage
- [ ] DNS for easy local domain names
- [ ] A nice dashboard to link everything together


## Software
- [OPNsense](https://opnsense.org) for routing
- [TrueNAS](https://www.truenas.com) for networked storage and backups (s3, NFS)
- [Proxmox](https://www.proxmox.com) For virtualization on nodes

## K8s Apps :material-kubernetes:
- [Homebridge](https://homebridge.io) for HomeKit control of _most_ smart devices
- [Zigbee2MQTT](https://www.zigbee2mqtt.io) for MQTT control of Zigbee devices[^1]
- [Zwavejs2MQTT](https://github.com/zwave-js/zwave-js-ui) for MQTT control of Zwave devices[^1]
- [Grafana](https://grafana.com) for dashboards
- [Prometheus](https://prometheus.io) for monitoring
- [InfluxDB](https://www.influxdata.com) for storage
- [Omada Controller](https://www.tp-link.com/us/business-networking/omada-sdn-controller/omada-software-controller/) for AP management

[^1]: These applications will need to be stuck to the nodes with attached Zwave and Zigbee USB dongles!