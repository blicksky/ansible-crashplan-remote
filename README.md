# ansible-crashplan-remote

### How to use
This assumes that you have CrashPlan installed on a remote server as well as the local computer where you will be running ansible.

1. Install Ansible: http://docs.ansible.com/ansible/intro_installation.html
2. Edit the `inventory` file to replace `<CRASHPLAN_SERVER_HOST>` with the hostname or address of your CrashPlan server.
3. Set up SSH key authentication for your CrashPlan server.
4. Run `ansible-playbook -i inventory playbook.yml --ask-sudo-pass`. This will establish an SSH tunnel.
6. Run the local CrashPlan UI.
7. When you're done, close the CrashPlan UI and close the SSH tunnel with `ctrl-C`.
