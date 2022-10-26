[![CI](https://github.com/de-it-krachten/ansible-role-asciinema_player/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-asciinema_player/actions?query=workflow%3ACI)


# ansible-role-asciinema_player

Set-up a webserver to hosts asciinema files



## Dependencies

#### Roles
None

#### Collections
- community.general
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- AlmaLinux 8
- AlmaLinux 9
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 35
- Fedora 36
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
  pre_tasks:
    - name: Create 'remote_tmp'
      ansible.builtin.file:
        path: /root/.ansible/tmp
        state: directory
        mode: "0700"
  roles:
    - nginx_docker
  tasks:
    - name: Include role 'asciinema_player'
      ansible.builtin.include_role:
        name: asciinema_player
</pre></code>
