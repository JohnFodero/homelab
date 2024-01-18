# Task Breakdown

## Stage 0: Prep :woman_in_lotus_position_tone1:

- [x] Set up rack with switch, UPS
- [x] Build router on HP 600 G3 (SFF)
- [x] Set up a few devices in new network
- [x] Design 3D printed rack mount for HP SFF PCs
- [ ] Design 3D printed rack mount for Dell SFF
- [ ] Create (this) website for documentation
    - [x] Add GH actions automation for deployment
    - [ ] Add GH actions for PR requirements (spellchecker, secrets checking, etc)
    
## Stage 1: MVP :man_standing_tone3:
- [x] Install Proxmox on worker nodes
- [x] Port full home network over to OPNsense
- [x] Set up TrueNAS on HP SFF
- [x] Set up local DNS
- [ ] Set up k3s deployment
    - [x] Use Ansible to configure clients/workers
    - [ ] Do some test deployments
        - [ ] Mosquitto
    - [ ] Set up monitoring (unsure what service to use)

## Stage 2: Automate/Scale :woman_walking_tone5:
- [ ] Automate worker node deployment
- [ ] Integrate GitOps
- [ ] Move current suite of docker services to k3s (my "Prod" environment)

## Stage 3: Add new services :man_running_tone1:
- [ ] [New services go here]
- [ ] Learn website dev through selfhosted webpage
- [ ] Set up power saving options

## Stage X: Bonus :people_with_bunny_ears_partying:
- [ ] Get disk shelf (that I got for free) working
- [ ] Design/implement power management
    - [ ] Implement device safe shutdown during power loss
    - [ ] Implement "peak pricing" usage reduction and battery backup cycle
- [ ] Set up self hosted GitHub agents