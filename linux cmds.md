# Ubuntu:

* Ubuntu is an open source Linux operating systems that runs on desktops, laptops, server and other devices…

* On Ubuntu, applications are available in two formats:

    1. Snap packages
    2. Debian packages.

* If an app is available in both formats, Ubuntu Software list the snap apps first.


# Uninstall Packages via Command Line

1. list all installed package
 >  sudo apt list --installed
2. To remove a package you find on the list
 >  sudo apt remove package_name
3. To uninstall multiple packages
 > sudo apt remove package_name_1 package_name_2
4. To completely remove packages and their configuration settings file
 > sudo apt purge package_name
5. to list snap packages
 >snap list
6. to remove snap packages
 > sudo snap remove package_name



# General Utility Commands Linux;

1.  echo:

```
echo with -e command used for
for tab; \t
for new line; \n
for escape sequence; \c
``` 

2.  if its a multi user system(to know user)=> who am I
3.  change passowd=> passwd
4.  show date:
 ```
 date
 Time +%T
 Hour +%H
 year +%Y
```

# Files & Directory


* files are 3 types
    1. regular file
    2. directory
    3. device files
* liux file system tree
* when we login in linux by default its in HOME directory(Folder)
* presente working dir= pwd
* change directory=  cd
* top node denoted by= /
* . current dir
*  .. perent dir(Folder) of curnt dir
*  create dir= mkdir
*  remove dir= rmdir
* Home Directory $HOME
* list files& directories=> ls
* list all files=> ls --all
* to create a file=> cat>file_name
* to over-write into a existing file=> cat>>file_name
* it gives file permision&user=> ls -l



# To know installed sw with dates:


> aptitude -F' * %p -> %d ' --no-gui --disable-columns search '?and(~i,!?section(libs), !?section(kernel), !?section(devel))'
> grep " install " /var/log/dpkg.log
> grep " install " /var/log/dpkg.log.1
> for app in /usr/share/applications/*.desktop; do echo "${app:24:-8}"; done
