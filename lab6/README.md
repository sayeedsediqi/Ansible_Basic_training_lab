Handlers
====

This lab introduces the use of handlers.  Handlers are actions that you may want to perform after all tasks have been executed in your play.  Within each task, you can use the notify flag to call a handler.  When Ansible determines a change has been made and you have specified to notify a handler, the hander will execute once all the tasks in the play have completed. 


An example where this could be useful is needing to update a configuration file on multiple web servers. If the configuration file is different then what you have defined, it will perform the described updates and could perform an action such as restarting a web service.

<br>


Playbook execution
---

ansible-playbook lab8.yml -i inventory.ini  --ask-vault-pass

