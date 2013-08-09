# UBUNTU

+ `upgrade: in a terminal` 
+ `do-release-upgrade -d`

and later (after update/upgrade)

`do-release-upgrade`

## USERS

List all users: `cat /etc/passwd` or `lastlog` which will give you a list of every single user plus the last time they logged in (or "never logged in" if that user had not logged in ever). 

+ Add user to group: `usermod -a -G desiredgroup myusername`
+ change user group `sudo chown -R username:group directory`
+ Change password `sudo passwd USERname`

## SERVER

Find current IP on which server "sits"

`ifconfig` and/or `ifconfig -a`

### Security

http://www.thefanclub.co.za/how-to/how-install-apache2-modsecurity-and-modevasive-ubuntu-1204-lts-server

http://www.thefanclub.co.za/how-to/how-secure-ubuntu-1204-lts-server-part-1-basics

### VirtualHost

Seting up hostname (Optional) https://library.linode.com/getting-started#sph_setting-the-hostname

For virtualbox we can leave default as host https://library.linode.com/hosting-website#sph_web-server So You'll need just to change `VirtualHost` Leaving `DocumentRoot /var/www` as is witout 
```
  ServerName  www.example.com
  ServerAlias example.com
```

## PHP

### 5.5.x

If timezone is "wrong", look for php.ini `sudo php -i | grep 'Configuration File'`

## FTPS

https://help.ubuntu.com/10.04/serverguide/ftp-server.html

`sudo apt-get install vsftpd`

### cURL

`sudo apt-get install php5-curl` or `sudo apt-get install curl libcurl3 libcurl3-dev php5-curl`

## MySQL

### phpMyAdmin

`sudo apt-get install phpmyadmin`

1. A symlink must be missing. Try to create one: `sudo ln -s /usr/share/phpmyadmin /var/www`
2. Change apache’s configuration file: `sudo gedit /etc/apache2/apache2.conf` add the following line to the conf file: `Include /etc/phpmyadmin/apache.conf`

After each modification, you may want to restart apache. To do so, use the following command: `sudo service apache2 restart`

## Shell /bash scripting

http://www.freeos.com/guides/lsst/index.html

# Symfony

## Configuration

http://www.joelverhagen.com/blog/2011/05/how-to-configure-symfony-2-0-on-ubuntu-server-2011-4/ 

## Tutorials

Creating a blog in Symfony2 http://tutorial.symblog.co.uk/ 

+ http://software-talk.org/blog/2012/06/symfony2-tutorial-for-beginners/ 
+ http://www.ricardclau.com/2011/09/littleweb-a-small-project-in-symfony2-chapter-1-translations/ 
+ http://ipsum.knplabs.com/ 
+ http://knpuniversity.com/screencast/question-answer-day/symfony2-users-menu-cms 

# Sphinx

http://acidborg.wordpress.com/2009/11/22/how-to-install-and-configure-sphinx-in-ubuntu-9-10-with-mysql-support/  

# OTHER

Not realy needed currently, but good to keep in mind

git@github.com:tv42/gitosis.git
