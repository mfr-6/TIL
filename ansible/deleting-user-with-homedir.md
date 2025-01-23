### Deleting multiple users with associated homedirs on target Linux machine
---

In order to remove users from target Linux machine you can use the following - very simple - Ansible Playbook:

```
---
- name: Remove users from the list
  hosts: all
  become: true
  tasks:
    - name: "Remove users with homedir"
      ansible.builtin.user:
        name: "{{ item }}"
        state: absent
        remove: yes
      loop:
         - example_user1
         - example_user2
      loop_control:
        label: "Removing user: {{ item }}"
```

- `remove: yes`: means removing associated directories with the user being deleted, for example home directory.
- `loop_control - label`: allows you to limit the output shown at each iteration. Very useful when iterating over huge datasets.