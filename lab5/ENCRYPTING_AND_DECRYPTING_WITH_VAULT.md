
Requirements for encrypting your password guide
----


ansible-vault encrypt group_vars/windows.yml 

ansible-vault view group_vars/windows.yml 

ansible-vault encrypt group_vars/windows.yml (encrypt the password) 

ansible-vault edit windows.yml 

ansible-inventory -i hosts --list --ask-vault-pass  

--- 

echo -n ‘<password>' | ansible-vault encrypt_string --stdin-name 'ansible_password' 

----


Update the passwrod value with encrypted password
-------

ansible_user: ansible 

ansible_password: !vault | 

$ANSIBLE_VAULT;1.1;AES256 

36356230663365626165396563623334333164313162306430373862333838636638333735393632 

6633626333363163623035343538363632373261636663610a663335633333346238333264383465 

33643334383266333235333366386539383737643136323736636333633834663037363666303962 

3138323239636561340a346439623364626662303833366532336533613864316266643564656430 

32393764653437323534646336666235373162643731303862353564386534326234 

ansible_winrm_server_cert_validation: ignore 

ansible_connection: winrm 



Decrypt the vault.
------

ansible-vault decrypt group_vars/windows.yml 



