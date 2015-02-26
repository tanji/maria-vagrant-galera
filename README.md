# maria-vagrant-galera
Vagrantfile with Ansible provisioner for MariaDB Cluster + MaxScale

This Vagrantfile starts a three node MariaDB Cluster and a MaxScale proxy instance with read connection routing already configured.

To connect to your newly started cluster:
<pre>$ mysql -umaxuser -pmaxpwd -h 192.168.50.104 -P4008</pre>
