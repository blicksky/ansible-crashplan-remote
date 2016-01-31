# ansible-crashplan-remote

### How to use
This assumes that you have CrashPlan installed on a remote server as well as the local computer where you will be running ansible.

1. Install Ansible: http://docs.ansible.com/ansible/intro_installation.html
2. Edit the `inventory` file to replace `<CRASHPLAN_SERVER_HOST>` with the hostname or address of your CrashPlan server.
3. Set up SSH key authentication for your CrashPlan server.
4. Run `ansible-playbook -i inventory playbook.yml`.
5. Set up an SSH tunnel to the CrashPlan server using something like `ssh -L 4200:localhost:4243 <CRASHPLAN_SERVER_HOST>`.
6. Run the local CrashPlan UI.
