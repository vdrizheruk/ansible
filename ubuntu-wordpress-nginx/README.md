## WordPress+Nginx+PHP-FPM Deployment On Ubuntu Server

- Requires Ansible 1.2 or newer
- Expects Ubuntu >= 14.04 hosts

These playbooks deploy a simple all-in-one configuration of the popular
WordPress blogging platform and CMS, frontend by the Nginx web server and the
PHP-FPM process manager. To use, copy the `hosts.example` file to `hosts` and 
edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Then run the playbook, like this:

	ansible-playbook -i hosts run.yml

The playbooks will configure MySQL, WordPress, Nginx, and PHP-FPM. When the run
is complete, you can hit access server to begin the WordPress configuration.

### Ideas for Improvement

Here are some ideas for ways that these playbooks could be extended:

- Parameterize the WordPress deployment to handle multi-site configurations.
- Separate the components (PHP-FPM, MySQL, Nginx) onto separate hosts and 
handle the configuration appropriately.
- Handle WordPress upgrades automatically.

