# maria-vagrant-galera
Vagrantfile with Ansible provisioner for MariaDB Enterprise Cluster + MaxScale

Supports: RHEL/CentOS and Debian/Ubuntu

This Vagrantfile starts a three node MariaDB Enterprise Cluster and a MaxScale proxy instance with read connection routing already configured.

For now, only one variable needs to be configured: `download_token` in vars/main.yml under the maxscale and galera roles.

To connect to your newly started cluster:
<pre>$ mysql -umaxuser -pmaxpwd -h 192.168.50.104 -P4008</pre>
