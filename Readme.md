# How it Works
This is my skeleton of odoo repository to start development Odoo CE and Odoo EE.

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

## Submodule Update
Adding Odoo Repository to deploy and autocomplete, also you can add all your repositories.

```bash
$ git submodule update --init --recursive --depth=10
```
