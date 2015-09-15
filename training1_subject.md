---
title: Training 1 - Vagrant
author: Loïc Delestra
header-includes:
    - \usepackage{fancyhdr}
    - \pagestyle{fancy}
    - \fancyhead[CO,CE]{Training 1 - Vagrant}
geometry: margin=2cm
---

##A/ First steps with Vagrant
@. Create a project folder 'vagrant\_first'
@. Create a Vagrantfile in your project (use a vagrant command)
@. Edit your vagrantfile to use a precise64 boxe.
@. Start your VM project and ssh into it
@. Install vim and apache2 (take notes about commands used)
@. Take a look at your apache default site configuration
@. Check your apache server is running (maybe try with a command for listing process)
@. Use the host machine browser to look at the apache default website.
@. **Call the teacher to check with you.**


##B/ Vagrant provisionning
You will need to provision your VM with some applications to use it.
As you work in team, you need to be sure your vagrant can be recreate from scratch with one command.
`vagrant up`

@. Create a new project folder called 'vagrant\_apache'
@. Use a precise64
@. At project root directory create a new folder architecture "sites/default/"
@. Add an index.html file in sites/default/
@. At project root directory create a provision script bootstrap.sh (edit Vagrantfile to use it)
@. bootstrap.sh must install apache2 and create links to redirect apache default site to /vagrant/sites/default/ (in guest vm)
@. Check everything is working from browser in host machine
@. Be sure you can destroy and recreate VMs with juste vagrant up.
@. **Call the teacher to check with you.**

##C/ Virtualhost
One vagrant, One apache, Two sites.

@. Create a new project folder 'vagrant\_virtualhost'
@. Use a provision script juste like before
@. This time your will not use apache default site configuration. You will have to create two configuration files. One for each virtualhost
Use licadmin-site1.conf and licadmin-site2.conf.
Your sites will use domaine name licadmin-site1.com and licadmin-site2.com.
Source code will be in sites/licadmin-site1 and sites/licadmin-site2 into the project folder (host)
Use different content in your index.html pages for each site.
@. Check your two sites are accessible from your host browser
@. Check your project is destroy prouf
@. **Call the teacher to check with you.**

##D/ PHP and Mysql
@. Create a new project folder 'vagrant\_amp'
@. Edit your provision script to install php5
@. Check php is enable and working by using an index.php page

###Bonus
@. Install a mysql database. Create tables you need and populate your DB when provisioning the VM.
@. For this... use your imagination
@. **Call the teacher to check with you.**

##E/ Package
**Package your A,B,C and D projects folder in a tar.gz archive and mail it to edu@delestra.com ^^**


