# Script
 Location I put my bash script
---

<!-- TOC -->
1. [createtp.sh](createtp.sh) will create KVM template but only for below OS;
* Available OS templates:
* alma-8.5                 x86_64     AlmaLinux 8.5
* centos-7.8               x86_64     CentOS 7.8
* centos-8.2               x86_64     CentOS 8.2
* debian-12                x86_64     Debian 12 (bookworm)
* ubuntu-20.04             x86_64     Ubuntu 20.04 (focal)
* fedora-32                x86_64     Fedora® 32 Server


<!-- TOC -->
---
2. [snapshot.sh](snapshot.sh) will create a snapshot of the VM. It can be used as a cronjob.

Sample command:
```shell
[root@vz ~]# ./snapshot.sh
Domain snapshot alma8 2023-10-11-15:20 created
Domain snapshot alma81 2023-10-11-15:20 created
Domain snapshot opensuse 2023-10-11-15:20 created
```
<!-- TOC -->
---
3. [get_pod_logs.sh](get_pod_logs.sh) Bash script that allows you to input a different pod name to check their log.

* Open your terminal.
* Create a new bash script file. For example, you can name it 'get_pod_logs.sh'
* Make the script executable
* Now you can use the script to get the logs of any pod by providing the pod name as an argument. For example, to get the logs of a pod named example-pod, you would run:
```shell
./get_pod_logs.sh example-pod
```

<!-- TOC -->
---
4. The [add_ssl_certificate.sh](add_ssl_certificate.sh) script automates the process of obtaining and configuring SSL certificates for domains using Let's Encrypt.

Features
* Requests SSL certificates for specified domains.
* Automatically updates the Apache ssl.conf with the new domain's configuration.
* Backs up the existing configuration before modifications.
* Validates the Apache configuration.
* Restarts Apache to apply changes.

Usage
* Ensure you have Certbot installed and Apache is configured.
* Prepare a file named domains.txt containing the domains you want to secure, one per line.
* Run the script with sudo privileges if you use Ubuntu:
```shell
sudo ./add_ssl_certificate.sh

```
* Follow the prompts or verify the output for any errors.


