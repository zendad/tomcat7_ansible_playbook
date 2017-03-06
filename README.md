## Standalone Tomcat Deployment to ubuntu Os

- Requires Ansible 1.2 or newer
- Expects Ubuntu hosts
- Install Openjdk 1.8
- Install Tomcat7

These playbooks deploy a very basic implementation of Tomcat Application Server,
version 7. To use them, first edit the "hosts" inventory file to contain the
hostnames of the machines on which you want Tomcat deployed, and edit the
group_vars/tomcat-servers file to set any Tomcat configuration parameters you need.

Then run the playbook, like this:

For Tomcat:

	ansible-playbook -i --user=ubuntu hosts/hosts site.yml
	
When the playbook run completes, you should be able to see the Tomcat
Application Server running on the ports you chose, on the target machines.

