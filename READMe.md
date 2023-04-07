# 1. General Purpose Utility commands in linux
- cat
- date
- echo
- printf
- bc
- script
 
# 2. ['Email Basics'](#Email) 
- mailx
- passwd
- who
- username
- tty
- stty

# 3. File management commands 
#### File handling
- cat
- cp
- rm
- more
- file
- wc -l, -w, -c
- od
- cmp
- comm
- diff
- gzip & gunzip -r, -d = compressing and decompressing files
- tar -c, -x, -t =disk archive
- zip 7 unzip
- find
- unmask

# 4. create a file in linux
- touch
- cat >
- vi
- vim
- nano

 # 5. Filters (to search)
 ##### filtering using RE
 1. grep: used to find words, text strings, number strings, or any other information in a single file or multiple files. 

   
    > **syntax :**  grep [options] word|”string” filename1 filename2 
   
    - -i	Ignore case in search results.
    - -w	Find only the whole words.
    - -v	Display non-matching lines.
    - -n	Display line number for matching lines.
    - -r	Perform recursive search.
    - -l	Print only the file names.
    - -c	Show only a count of the number of matches.
    - --color	Highlight matched string in different colors.

    > **ex: grep Linux sample.txt**

  2. egrep
  3. sed: stream editor 

# 6. Adv Filters

#### 6. awk: 
  - awk is a command-line utility as well as a scripting language.
  - that is used to manipulate data and format output reports.
  - This command supports several variables, functions, and logical operators to get the desired output.

    
    >  ***awk [options] 'selection_criteria {action}' input-file > output-file***
    

# 7. Filters
- pr
- head
- tail
- cut
- paste
- sort
- uniq
- tr

# 8. linux commands classified into 2 categories

##### Internal(SHELL) commands:(alredy loaded in SHELL)
- built into shell
- to view type --help in bash
##### External(KERNAL) commands:(loaded when user req for them)
- built into kernal 
- stored in /bin or /sbin 
- to execute these shell look into $PATH var 
- If cmnd present in that location SHELL will execute that or get error


***"type" is used to find out whether a command is internal or external?***
> **example:type cd**


# 9. How to control System and Services” on a system running systemd. 	

- Systemctl is a systemd utility that is responsible for Controlling the systemd system and service manager.
- Systemd is a collection of system mngmt daemons, utilities & ibraries 
- which serves as a replacement of System V init daemon. 
- Systemd functions as central management and configuration platform for UNIX like system.

> ***systemctl [OPTIONS...] COMMAND [NAME...]***
**Important:** 

Systemctl accepts 
- services (.service), 
- mount point (.mount), 
- sockets (.socket),
- devices (.device) as units.


# 10. MOUNTING:
Mounting refers to making a group of files in a file system structure accessible to user or group of users. 
It is done by attaching a root directory from one file system to that of another. 
This ensures that the other directory or device appears as a directory or subdirectory of that system.

Mounting may be local or remote. 
In local mounting it connects disk drivers as one machine such that they behave as single logical system,while remote mount uses NFS(Network file system) to connect to directories on other machine so that they can be used as if they are the part of the users file system




 


