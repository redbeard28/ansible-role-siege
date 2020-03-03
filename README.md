ANSIBLE-ROLE-SIEGE
==================

Ansible role install Siege http load and benchmarking utility from Joe DOG dev.


## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: redbeard28.siege
````

More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible 2.9+


Role Variables
--------------

```yaml
---
siege_remove_distro_version: true
siege_param_nofollow_url:
  - {name: "doubleclick", url: "ad.doubleclick.net"}
  - {name: "pagead2.googlesyndication", url: "pagead2.googlesyndication.com"}
  - {name: "ads.pubsqrd", url: "ads.pubsqrd.com"}
  - {name: "ib.adnxs", url: "ib.adnxs.com"}
```

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redbeard28.siege, tags: mytags }


Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
image=debian tag="buster" molecule converge 
image=debian tag="buster" molecule verify 
```

Author Information
------------------

Jeremie CUADRADO[¹](mailto:info@redbeard-consulting.fr) from Redbeard-Consulting
