Updating files
====
This lab introduces the file and win_file module in Ansible.  

In this lab, you will notice we are pulling output from the facts that were gathered on the endpoints.

On the Windows system, we are able to locate the user account of the logged in user by checking the environment variable and looking at the USER key.  {{ ansible_facts['env']['USERNAME'] }}.

<br>

Playbook execution
---

ansible-playbook lab3.yml -i inventory.ini --ask-vault-pass