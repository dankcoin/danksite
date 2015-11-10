##Contributing to dankcoin.org (Linux Guide)



###Note:
This guide only covers Debian & Ubuntu.
If you use RHEL, Fedora, Arch, etc, you should have enough knowledge to install the packages yourself.

###Step 1: Set-up a webserver

Before you start, you will need a webserver. The most common webservers are **Apache** and **NGINX**.

We'll build and use a LAMP-Stack (**L**inux **A**pache **M**ySQL **P**HP) in our Guide.

First install the needed packages:

Open a terminal and execute:

    sudo apt-get install apache2 libapache2-mod-php5 php5 php5-mysql mysql-server 
    
or
    
    sudo aptitude install apache2 libapache2-mod-php5 php5 php5-mysql mysql-server 

While installing, the console will ask you to set a password for the mysql user.
Because this is a local testing system, you can set the password to something simple like `root` or `1234`.

After the installation process is finished, open a browser and go to [http://localhost](http://localhost) or http://127.0.0.1.

If you see something like this, everything is ready:
    
    It works!

    This is the default web page for this server.

    The web server software is running but no content has been added, yet.
  
If you don't see the message above, try to manually start Apache. Open a terminal and execute:

    sudo service apache2 start 

or

    sudo /etc/init.d/apache2 start
    
Now you're ready to start :smiley:

##Step 2: Clone the danksite repo

To clone the danksite repository you'll need GIT.

To install GIT, open a terminal and execute:
  
    sudo apt-get install git

or

    sudo aptitude install git
    
If you cannot install **git** use the package **git-core** instead.

Now you're ready to clone.

<br />

Go into your webserver directory:

Note: The path depends on your Apache Version.

For Apache 2.4+ use:

    cd /var/www/html

For any older version use:

    cd /var/www
    
Now clone the repo (cloning will create the subdirectory `danksite`)

    git clone https://github.com/dankscoin/danksite.git dankcoin
    
##Step 3: Happy Coding :)

Now you have a working copy of [dankcoin.org](http://dankcoin.org) at [http://127.0.0.1/dankcoin](http://127.0.0.1/dankcoin).

Just point your favourite IDE or Editor to `/var/www/dankcoin` or `/var/www/html/dankcoin` and start editing.
