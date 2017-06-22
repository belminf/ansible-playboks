Collection of personal Ansible playbooks.

# Install
## OS specific
### Cygwin
Assuming [apt-cyg](https://github.com/transcode-open/apt-cyg) installed.

    $ apt-cyg install gcc-core openssl-devel
    $ export CFLAGS="-D_DEFAULT_SOURCE"

### Ubuntu
    $ sudo apt-get update && sudo apt-get install -y libssl-dev python-pip

## Python
    $ pip install -r requirements.txt

# Playbooks
Example of running on one host:
    $ ansible-playbook --check -i 192.168.5.55, playbooks/raspberry_pi.yaml 


## raspberry_pi
* Installs Plex Media Server
