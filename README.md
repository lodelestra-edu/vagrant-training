# Training 1 - Vagrant

## A/ First steps with Vagrant
1. Create a project folder 'vagrant\_first'
2. Create a Vagrantfile in your project (use a vagrant command)
3. Edit your vagrantfile to use a ubuntu/trusty64 boxe.
4. Start your VM project and ssh into it
5. Install vim and apache2 (take notes about commands used)
6. Take a look at your apache default site configuration
7. Check your apache server is running (maybe try with a command for listing process)
8. Use the host machine browser to look at the apache default website.


## B/ Vagrant provisionning
You will need to provision your VM with some applications to use it.
As you work in team, you need to be sure your vagrant can be recreate from scratch with one command.
`vagrant up`

1. Create a new project folder called 'vagrant\_apache'
2. Use a ubuntu/trusty64
3. At project root directory create a new folder architecture "sites/default/"
4. Add an index.html file in sites/default/
5. At project root directory create a provision script bootstrap.sh (edit Vagrantfile to use it)
6. bootstrap.sh must install apache2 and create links to redirect apache default site to /vagrant/sites/default/ (in guest vm)
7. Check everything is working from browser in host machine
8. Be sure you can destroy and recreate VMs with juste vagrant up.
9. **Call the teacher to check with you.**

## C/ Virtualhost
One vagrant, One apache, Two sites.

1. Create a new project folder 'vagrant\_virtualhost'
2. Use a provision script juste like before
3. This time your will not use apache default site configuration.
You will have to create two configuration files. One for each virtualhost. Use licadm\_site1.conf and licadm\_site2.conf.
Your sites will use domaine name licadm\_site1.com and licadm\_site2.com.
Web site source code will be in `sites/licadm_site1` and `sites/licadm_site2` into the project folder (host).
Use different content in your index.html pages for each site.
4. Check your two sites are accessible from your host browser
5. Check your project is `vagrant destroy` proof
6. **Call the teacher to check with you.**

## D/ PHP and Mysql
1. Create a new project folder 'vagrant\_amp'
2. Edit your provision script to install php5
3. Check php is enable and working by using an index.php page
4. Install a mysql database. Create tables you need and populate your DB when provisioning the VM.
5. For this... use your imagination
6. **Call the teacher to check with you.**

## E/ Package
**Package your B and C projects folder in a tar.gz archive and mail it to edu@delestra.com ^^**

