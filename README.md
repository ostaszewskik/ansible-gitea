Ansible-Gitea
=========

The real challenge is not installing it, but configuring it properly. The official documentation is lacking some key components - in particular regarding configuring reversed proxy in webserver. 


More information [here](https://mindefrag.net/2018/07/how-to-install-and-configure-gitea-a-self-hosted-github-like-service/)

Requirements
------------

* LAMP stack
* Ansible > 2.0
* root privileges

Role Variables
--------------

Define those variables outside role folder:

* group_srv_domain (domain of your server)
* group_srv_admin_mail (your admin email)


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - gitea

Define hosts in hosts file. Run:

**ansible-playbook -i hosts playbook.yml**

to provision


run:

**ansible-playbook -i hosts playbook.yml --tag "uninstall"**

to delete all files, users and groups and cronjobs created during this configuration 

