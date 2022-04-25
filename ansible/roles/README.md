ansible-nginx-docker-compose
============================

Ansible role to deploy nginx on a container managed by docker-compose.
Nginx is configured to use SSL/TLS using a self signed certificate or a
Let's Encrypt certificate (obtained with certbot).

Requirements
------------

None

Role Variables
--------------

See [`defaults/main.yml`](./defaults/main.yml)

Dependencies
------------

None

Install Playbook
----------------

---
- name: Install foundry
  hosts: localhost
  #connection: ssh
  become: true
  become_method: su
  become_exe: 'sudo su -'
  become_user: root
  remote_user: vagrant
  roles:
    - docker_install
```

Install Foudry
----------------

---
- name: Install foundry
  hosts: localhost
  #connection: ssh
  become: true
  become_method: su
  become_exe: 'sudo su -'
  become_user: root
  remote_user: vagrant
  roles:
    - foundryvtt
    

Install Jenkins
----------------

 ---
- name: Install foundry
  hosts: localhost
  # connection: ssh
  become: true
  become_method: su
  become_exe: 'sudo su -'
  become_user: root
  remote_user: vagrant
  roles:
    # - docker_install
    - jenkins
