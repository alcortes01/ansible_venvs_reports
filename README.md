# Python Virtual Environments Report Generator 
The purpose of the Ansible playbook get_venv_info.yml is to generate a CSV report and individual requirements.txt files with hostname suffix. The CSV file can be opened with a spreadsheet program like Excel. The *.requirements.txt files can be used to install Python packages using the tool PIP. 

Notice: The Ansible playbook will look for the Python virtual environments created in the directory /var/lib/awx/customEnv. If you have any other path, modify the tasks in the playbook to match the path you want. 
## Usage 
Create your "inventory" file with the remote host you want in your reports. 

Use ansible-playbook command to execute: 
```
ansible-playbook -i inventory -u userID -k: --ask-become-pass get_venv_info.yml 
```
Notice that you need to change the "userID" with your own login ID used to SSH the remote host. The parameter -k will ask for your SSH password. 
