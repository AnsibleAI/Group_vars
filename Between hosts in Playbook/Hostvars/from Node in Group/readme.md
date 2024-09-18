sch: https://www.google.com/search?q=ansible+hostvars+groups

# Works!:
https://serverfault.com/questions/615132/accessing-hostvars-for-a-host-group-in-ansible

uni.yml
```
- hosts: desktop #localhost
  tasks:
  - ansible.builtin.debug:
      msg: "{{ ansible_default_ipv4.address }}"
  
- hosts: server
  tasks:
  - debug:
      msg: "Default IP: {{ hostvars[item]['ansible_default_ipv4']['address'] }}"
    with_items: "{{ groups['desktop'][0] }}"
```
