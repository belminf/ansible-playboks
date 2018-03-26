Collection of personal Ansible playbooks.

# Install
## OS specific
### Ubuntu
    $ sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-pip

## Python
    $ pip install -r requirements.txt

# Playbooks
* `personal_setup.yml` - Setup for my personal boxes
* `ubuntu_bootstrap.yml` - Bootstrapping Ubuntu for Ansible

## Example playbook runs
Only apply to one instance:

    $ ansible-playbook playbooks/personal_setup.yaml -l pi

Only apply `vim` updates:

    $ ansible-playbook playbooks/personal_setup.yml -t vim
