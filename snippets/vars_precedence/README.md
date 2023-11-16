Ansible variables
=================

Sample playbook, to show variable precedence in Ansible:


Sample
-----

1. Run the playbook with the code snippet below
2. Find the place, where the variable is defined and why it overwrites another one
3. Then run the playbook again to see which other variable is printed out
4. Repeat the steps until you get the variable with the highest priority


Run the playbook
----------------

```
$ ansible-playbook -i hosts -l localhost -e '{ "xxx": "This value is passed through command-line" }' ./site.yaml
```


Hints
----------

Remember, here is the original order of the priority of variables in Ansible:

Also see the original documentation: https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable

> 1. command line values (for example, `-u my_user`, these are not variables)
> 2. role defaults (defined in role/defaults/main.yml) 
> 3. inventory file or script group vars 
> 4. inventory group_vars/all 
> 5. playbook group_vars/all 
> 6. inventory group_vars/* 
> 7. playbook group_vars/*
> 8. inventory file or script host vars 
> 9. inventory host_vars/* 
> 10. playbook host_vars/* 
> 11. host facts / cached set_facts 
> 12. play vars
> 13. play vars_prompt
> 14. play vars_files
> 15. role vars (defined in role/vars/main.yml)
> 16. block vars (only for tasks in block)
> 17. task vars (only for the task)
> 18. include_vars
> 19. set_facts / registered vars
> 20. role (and include_role) params
> 21. include params
> 22. extra vars (for example, `-e "user=my_user"`)(always win precedence)

