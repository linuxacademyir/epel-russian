# epel-russian
how to setup epel repository for countries with sanction centos 7
replace your DNS with a Russian DNS server by removing resolv.conf file and creating a new one 
$ sudo rm -rf /etc/resolv.conf
$ sudo vim /etc/resolv.conf
insert in this file
nameserver 77.88.8.8
Now rename the actul Cetnos Base Repo by this command
$ sudo mv CentOS-Base.repo etc/yum.repos.d/CentOS-Base.repo_back
now create a and open  repo file by 
$ sudo vim /etc/yum.repos.d/Epel-Centos7.repo 
 and update 
$ sudo yum update -y 
 now install any packages, for example to install openvpn 
$ sudo yum install openvpn 
