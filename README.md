## Quickly bootstrap new installation to a usable state

**WIP**

Main goal is to just run the playbooks and have a ready environemnt with basic development tools and their configurations.


## Running the notebooks

### Prequsites

You need to have ansible and its dependencies installed. To do so run

Ubuntu
`sudo apt update && sudo apt install ansible`
Arch
`sudo pacman -S ansible`

`ansible-galaxy install -r ./collections/requirements.yml`

To run the notebook first prepare the configuration file

`cp -r inventory/sample inventory/my-config`

Inside the `my-config` catalog specify your hosts in `hosts.ini` file ( you can also use localhost as it specified in the example ).

Possible configuration targets:
* `ubuntu`
* `arch`
* `terminal`

Also inside `group_vars/all.yml` specify you `ansible_user`, `timezone` and the preferred `system`

After that just run

`./deploy.sh`


### Tools

Web
- npm
- yarn

Shell
- fish
- tmux
- nvim


Other
- docker


### Support

Planned support for
- Ubuntu
- Arch
