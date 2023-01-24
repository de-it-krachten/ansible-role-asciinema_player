[![CI](https://github.com/de-it-krachten/ansible-role-asciinema_player/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-asciinema_player/actions?query=workflow%3ACI)


# ansible-role-asciinema_player

Set-up a webserver to hosts asciinema files



## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8<sup>1</sup>
- RockyLinux 9<sup>1</sup>
- OracleLinux 8<sup>1</sup>
- OracleLinux 9<sup>1</sup>
- AlmaLinux 8<sup>1</sup>
- AlmaLinux 9<sup>1</sup>
- Debian 10 (Buster)<sup>1</sup>
- Debian 11 (Bullseye)<sup>1</sup>
- Ubuntu 18.04 LTS<sup>1</sup>
- Ubuntu 20.04 LTS<sup>1</sup>
- Ubuntu 22.04 LTS<sup>1</sup>
- Fedora 36<sup>1</sup>
- Fedora 37<sup>1</sup>
- Alpine 3<sup>1</sup>
- Docker dind (CI only)

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'asciinema_player'
  hosts: all
  become: "yes"
  vars:
    asciinema_fqdn: asciinema.example.com
    asciinema_cast_path: files
    asciinema_html_path: /export/docker/nginx/html
  roles:
    - nginx_docker
  tasks:
    - name: Include role 'asciinema_player'
      ansible.builtin.include_role:
        name: asciinema_player
</pre></code>
