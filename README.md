# automysqlbackup
A fork of AutoMySQLBackup script from sourceforge. http://sourceforge.net/projects/automysqlbackup/

This repo is used as source for an Ansible role to configure Automysqlbackup.
Although Automysqlbackup is available through many package managers the version supplied is 2.5 not 3.
Three has better features.

Changes from the original release are to add --events to the dump commande to avoid errors. (made by masche842)

Also in the role we grant EVENT privileges to the DB user running the role to stop the error:

````
mysqldump: Couldn't execute 'show events': Access denied for user
````
