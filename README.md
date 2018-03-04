Collection of personal Ansible playbooks.

# Install
## OS specific
### Ubuntu
    $ sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-pip

## Python
    $ pip install -r requirements.txt

# Playbooks
* `linux.yml` - My minimal Linux config
* `raspberry-pi.yml` - Raspberry Pi I use as a media box
* `ubuntu_bootstrap.yml` - Bootstrapping Ubuntu for Ansible
* `vps_workbench.yml` - My remote workbench

## Example playbook runs
### Local
Apply a role:

    $ ansible-playbook -i localhost, -c local playbooks/roles/vim.yml

### Remote
Apply a playbook

    $ ansible-playbook -i 192.168.3.200, playbooks/linux.yml

### Raspberry Pi

    $ ansible-playbook -i raspberrypi, --extra-vars 'transmission_ratio_limit=7.5' playbooks/raspberry-pi.yaml 
