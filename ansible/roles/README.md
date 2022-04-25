
Requirements
------------

None

Dependencies
------------

None

Install Playbook
```
---
- name: Install docker
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

``` 
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
 ```
 
 ```
 ---
- name: Install jenkins
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
```
