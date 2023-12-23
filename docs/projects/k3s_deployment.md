# Deploying K3s

There are so many great resources online, ranging from low-level, piece-by-piece deployments to fully automated, turn-key solutions. I am going to more automated route, following a series of tutorials from [Techno Tim](https://www.youtube.com/@TechnoTim) on YouTube. 

## Steps:

1. [Set up VMs on Proxmox](https://technotim.live/posts/cloud-init-cloud-image/)
    
    Configuration:
    - HP Mini 1 (32GB RAM)
        - 2x master nodes, 2 vCPU, 8GB RAM, 32GB disk
        - 1x worker node, 2 vCPU, 8GB RAM, 32GB disk
    - HP Mini 2 (8GB RAM)
        - 2x master nodes, 2 vCPU, 8GB RAM, 32GB disk
        - 1x worker node, 2 vCPU, 8GB RAM, 32GB disk
    
    This configuration allows for HA with 2 master nodes on each proxmox host. 

    Notes:

    - I do not currently have a Proxmox cluster set up between these two nodes. It would be nice from a management perspective to have a single interface to manage both nodes, but I would rather continue to build up features before exploring this.
    - Increased the scsi0 drive to ~32GB _prior_ to replicating the template. I originally used the default, and 2GB ran into issues during the next step when installing k3s.
    - Allocated 8GB of RAM for the template over the default 2GB.
    - Set up DHCP static IP in OPNsense LAN leases for each node.

2. [Set up Ansible](https://technotim.live/posts/ansible-automation/)
    
    Notes:
    - I utilized the [site.yml](../../ansible/site.yml) and [reset.yml](../../ansible/reset.yml) quite a bit when setting up my nodes. Between updating memory allocation, disk size and master/worker node allocation, having a method to reset the cluster, update the [hosts.ini](../../ansible/inventory/k3s_cluster_01/hosts.example.ini). 

3. [Set up K3s](https://technotim.live/posts/k3s-etcd-ansible/)

    Notes:
    
    - Unless you use the `master` and `node` tags in the [hosts.ini](../../ansible/inventory/k3s_cluster_01/hosts.example.ini), the playbook required some updating of the default master, node, and cluster tags in a few places to get all stages to get the correct host groups for each stage.

4. [Install Helm](https://rpi4cluster.com/k3s/k3s-helm-arkade-setting/)
    
    This one is easy.
    ```bash
    brew install helm
    ```

4. [Set up Longhorn]()
    
    This tutorial was a bit tailored to setup with Rancher, but the [Longhorn install](https://longhorn.io/docs/1.5.3/deploy/install/install-with-kubectl/) was more than sufficient to wask through what is required. 


## My First Deployment :) 

Mosquitto MQTT Broker

```bash
kubectl 
