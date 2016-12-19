# Mail-Migrate

This script is used to Migrate/Sync mail boxes between two servers/same servers regardless of which control panel they use. You do not need the server root access or any control panel access to migrate the email accounts. All you need to have the following things.

1. Source email [The email account on the source server that needs a migration]
2. Source email password.
3. Source server IMAP IP/Hostname
4. Destination email [To which email account the Souce email mailbox should be transferred]
5. Destination email password
6. Destination server IMAP hostname

The advantage of this method is, you do not need to install any packages/services on your Source or Destination server and you can run this script even from your personal laptop if its Linux flavoured. Before using this script,you should install the utility 'imapsync' on your Laptop/Test server from where you are running this.

It does not come by default on CentOS, you need to add EPEL repository.

CentOS 6
=========
wget http://dl.fedoraproject.org/pub/epel/6/i386/epel-release-6-8.noarch.rpm

rpm -Uvh epel-release-6-8.noarch.rpm

yum install imapsync

Ubuntu 14/15/16
===============

Refer : http://imapsync.lamiral.info/INSTALL.d/INSTALL.Ubuntu.txt


Step for a single email account migration :
==========================================
#imapsync --host1 server1.example1.com --user1 user@domain.com --password1 emailPassword --host2 server.exmaple2.com --user2 user@domain.com --password2 emailPassword 

Well, if you have a number of email accounts say 50 more then you can make use of my script. You need to enter email accounts,hostnames,passwords on seperate .txt files comes with this repository and run the bash script.

1. host1.txt [Enter source hostnames one by one, if yo have 10 emails then add hostname 10 times]
2. email1.txt [Enter email accounts one by one]
3. password1.txt [Enter respective email passwords per line]
4. host2.txt [Destination hostnames]
5. email2.txt [Email accounts, line by line]
6. password2.txt [Email account passwords on destination server]

