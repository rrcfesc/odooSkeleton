# How it Works
This is my skeleton of odoo repository to start development Odoo CE and Odoo EE.

## Configuration
Create a file called .odoorc and copy the content of .odoorc.dist

Create the follows Foldes:

    - odoo-repo
    - proyecto
    - addons-vauxoo
    - mexico
    - server-tools
    - database
    - enterprise

Why?

Because is the most common folder on México addons

### Odoo 11
You must be clone inside the odoo-repo folder the proyect Odoo version 11, one example of this is:

```bash
$ cd odoo-repo
$ git clone --single-branch --depth=10 https://github.com/odoo/odoo.git .
```

### Enterprise
Clone inside the folder enterprise the repository of enterprise

## Your Proyecto
Clone inside the folder "proyecto" your themas or modulos or proyects.

```bash
$ cd proyecto
$ git clone https://github.com/OWNER/REPOSITORY.git odoo-repo .
```

Example of .odoorc 
```
[options]
addons_path = /home/odoo/enterprise,/home/odoo/odoo-repo/addons,/home/odoo/server-tools,/home/odoo/mexico,/home/odoo/addons-vauxoo,/home/odoo/mymodules
admin_passwd = admin
data_dir = /home/odoo/.local/share/Odoo
db_host = odooskeleton_db
db_maxconn = 64
db_name = odooskeleton
db_password = passwd
db_port = False
db_sslmode = prefer
db_template = template1
db_user = odoo
db_filter = odooskeleton
demo = {}
email_from = False
without_demo = True
```


## How to use
Yo must login like this and change the user:

```bash
$ docker exec -it odooskeleton-odoo bash
root@random# su odoo
$ cd
$ ls -al
drwxr-xr-x  1 odoo odoo 4096 ago 27 21:54 .
drwxr-xr-x  1 root root 4096 ago 27 20:49 ..
-rw-r--r--  1 odoo odoo  220 ago 31  2015 .bash_logout
-rw-r--r--  1 odoo odoo 3771 ago 31  2015 .bashrc
drwxr-xr-x 22 odoo odoo  748 ago 27 18:31 odoo-repo
-rw-r--r--  1 odoo odoo  655 may 16  2017 .profile
drwx------ 20 odoo odoo  680 ago 22 20:20 .ssh
```

# Execute Odoo

```bash
$ ./odoo-repo/odoo-bin -c ~/config/odoo.conf
```
If you need update modules pass the parameters on this command line

@author Ricardo Ruiz <ricardojesus.ruizcruz@gmail.com>
