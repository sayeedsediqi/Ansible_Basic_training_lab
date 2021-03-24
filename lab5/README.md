Securing passwords
====

This lab introduces the use of securing passwords.  It gets tedious in having to enter your RBAC password every time you run a playbook but you want to avoid in having passwords stored in plain text.   This is where ansible-vault comes to the rescue.   This guide will walk you through how to make use of ansible-vault to store encrypted files in your playbooks. 

<br>

Guide
----

1. Execute the ansible playbook ansible_vault_setup.yml:  

<br>

Playbook execution
---

ansible-playbook ansible_vault_setup.yml --ask-vault-pass

