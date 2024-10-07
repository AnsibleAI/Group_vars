sch: https://www.google.com/search?q=ansible+get+ip+from+another+host
- https://www.google.com/search?q=ansible+ansible_default_ipv4+from+group+vars

# Solution:
## works:
https://forum.ansible.com/t/how-to-get-another-hosts-ip-hostname-from-the-inventory-as-a-variable/2125

```
- name: mongodb host
  debug:
    msg: "{{ groups['mongodb'][0] }}"
```

## Try:
https://stackoverflow.com/questions/36328907/ansible-get-all-the-ip-addresses-of-a-group
