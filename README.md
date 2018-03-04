Collection of personal Ansible playbooks.

# Install
## OS specific
### Ubuntu
    $ sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-pip

## Python
    $ pip install -r requirements.txt

# Playbooks
## Roles
* plex_media_server - Installs PMS using `dev2day.de` repo
* transmission - Installs and configures the Torrent client

## Example playbook runs
### Local
Apply a role:

    $ ansible-playbook -i localhost, -c local playbooks/roles/vim.yml

## Remote
Apply a playbook

    $ ansible-playbook -i 192.168.3.200, playbooks/linux.yml

### Raspberry Pi
All roles:

    $ ansible-playbook -i raspberrypi, playbooks/raspberry-pi.yaml 

Just Transmission role:

    $ ansible-playbook -i raspberrypi, --extra-vars 'transmission_ratio_limit=7.5' playbooks/raspberry-pi/transmission.yml
