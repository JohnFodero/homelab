# Start Here

## Goals
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


## Software
- [OPNsense]() for routing
- [TrueNAS]() for networked storage
- [Proxmox]() For virtualization on nodes

## K8s Apps
- [Homebridge]() for HomeKit control of _most_ smart devices
- [Zigbee2MQTT]() for MQTT control of Zigbee devices[^1]
- [Zwavejs2MQTT]() for MQTT control of Zwave devices[^1]
- [Grafana]() for dashboards
- [Prometheus]() for monitoring
- [InfluxDB]() for storage
- [Omada Controller]() for AP management

[^1]: These applications will need to be stuck to the nodes with the repective Zwave and Zigbee USB dongle!