# maria-vagrant-galera
Vagrantfile with Ansible provisioner for MariaDB Enterprise Cluster + MaxScale

Supports: RHEL/CentOS and Debian/Ubuntu

This Vagrantfile starts a three node MariaDB Enterprise Cluster and a MaxScale proxy instance with read connection routing already configured.

## General instructions

First of all clone this repository on your machine.

For now, only one variable needs to be configured: `download_token` in vars/main.yml under the maxscale and galera roles.
You will find your enterprise trial download token at http://www.mariadb.com/my_portal (login required)

Install vagrant, virtualbox and ansible.

Debian/Ubuntu:

```sudo apt-get install vagrant virtualbox ansible```

CentOS/RedHat:

```yum install vagrant virtualbox ansible```

Then to bring up your cluster:

```vagrant up```

To connect to your newly started cluster from your local machine:
```$ mysql -umaxuser -pmaxpwd -h 192.168.50.104 -P4008```

## If you need Ubuntu or Debian boxes

The default configuration uses CentOS boxes. If you want to use Ubuntu or Debian boxes replace the default `Vagrantfile` by `Vagrantfile.debian` or `Vagrantfile.ubuntu`
