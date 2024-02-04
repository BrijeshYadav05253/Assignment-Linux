# Assignment 4

  ### Question 1- Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.

```
brijesh@brijesh-Inspiron-5567:~$ sudo mkdir MyFiles
[sudo] password for brijesh: 
brijesh@brijesh-Inspiron-5567:~$ cd MyFiles/
brijesh@brijesh-Inspiron-5567:~/MyFiles$ ls
brijesh@brijesh-Inspiron-5567:~/MyFiles$ 

```

### Question 2- Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."

```
brijesh@brijesh-Inspiron-5567:~$ sudo touch document.txt
[sudo] password for brijesh: 
brijesh@brijesh-Inspiron-5567:~$ sudo cp document.txt MyFiles/
brijesh@brijesh-Inspiron-5567:~$ cd MyFiles/
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo mkdir Documents
brijesh@brijesh-Inspiron-5567:~/MyFiles$ cd Documents/
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ cd ..
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo mv document.txt Documents
brijesh@brijesh-Inspiron-5567:~/MyFiles$ ls
Documents
brijesh@brijesh-Inspiron-5567:~/MyFiles$ cd Documents/
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ ls
document.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ 
```

### Question 3- Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.

```
brijesh@brijesh-Inspiron-5567:~$ cd MyFiles/
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo touch notes.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles$ ls
Documents  notes.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo rm notes.txt 
brijesh@brijesh-Inspiron-5567:~/MyFiles$ ls
Documents
brijesh@brijesh-Inspiron-5567:~/MyFiles$ 
```

### Question 4- Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location. 

```
brijesh@brijesh-Inspiron-5567:~/MyFiles$ cd Documents/
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ ls
document.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ sudo ln document.txt hardlink.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ sudo ln -s document.txt symlink.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles/Documents$ 

```

### Question 5- In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.

```
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo touch aabb.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo touch accb.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles$ ls
aabb.txt  accb.txt  Documents
brijesh@brijesh-Inspiron-5567:~/MyFiles$ sudo ls a*.txt
aabb.txt  accb.txt
brijesh@brijesh-Inspiron-5567:~/MyFiles$ 

```

### Question 6- Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.

```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ rename -n 's/\.txt$/.bak/' *.txt
rename(abc.txt, abc.bak)
rename(def.txt, def.bak)
rename(ghi.txt, ghi.bak)
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ ls
aa.bak  abc.txt  bb.bak  cc.bak  def.txt  ghi.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ sudo rename -n 's/\.txt$/.bak/' *.txt
rename(abc.txt, abc.bak)
rename(def.txt, def.bak)
rename(ghi.txt, ghi.bak)
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ ls
aa.bak  abc.txt  bb.bak  cc.bak  def.txt  ghi.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ sudo rename 's/\.txt$/.bak/' *.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ ls
aa.bak  abc.bak  bb.bak  cc.bak  def.bak  ghi.bak
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ 
 

```
### Question 7- Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
```
brijesh@brijesh-Inspiron-5567:~/Home$ cd MyFiles/
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ cd Documents/
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ cd ..
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ cp Documents/* Backup/
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ ls Documents/
aa.bak  abc.txt  bb.bak  cc.bak  def.txt  ghi.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ ls Backup/
aa.bak  abc.txt  bb.bak  cc.bak  def.txt  ghi.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ 
```
### Question 8- Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ touch file1.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ ls
aa.bak  abc.bak  bb.bak  cc.bak  def.bak  file1.txt  ghi.bak
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ vim file1.txt 
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ grep '\.txt$' file1.txt 
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ 

```


### Question 9- Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ touch BaBa.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ vim BaBa.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ cat BaBa.txt 
My Name Is BABA
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ 
```
### Question 10- Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.
```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ vim BaBa.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ current_date=$(date); echo "Current Date: $current_date"; echo "$current_date" >> my_notes.txt
Current Date: Saturday 03 February 2024 08:58:36 PM IST
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ 
```
### Question 11- Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
```
brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ vim ~/.bash_profile root@:brijesh-Inspiron-5567/Home/MyFiles/Documents# cat ~/.bash_profile export CUSTOM_PATH="/Home/MyFiles"
6 files to edit
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ source ~/.bash_profile
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ echo $CUSTOM_PATH
/Home/Myfiles
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles/Documents$ 
```

### Question 12- Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ echo "This is a new line of text." >> my_notes.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ cat my_notes.txt
Saturday 03 February 2024 08:58:36 PM IST
This is a new line of text.
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ 

```
### Question 13- List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
```
brijesh@brijesh-Inspiron-5567:~$ ls /etc | grep "conf" > conf_files.txt
brijesh@brijesh-Inspiron-5567:~$ cat conf_files.txt
adduser.conf
apg.conf
appstream.conf
brltty.conf
ca-certificates.conf
ca-certificates.conf.dpkg-old
dconf
debconf.conf
deluser.conf
e2scrub.conf
fprintd.conf
fuse.conf
gai.conf
hdparm.conf
host.conf
insserv.conf.d
kernel-img.conf
kerneloops.conf
ld.so.conf
ld.so.conf.d
libao.conf
libaudit.conf
logrotate.conf
manpath.config
mke2fs.conf
netconfig
nftables.conf
nsswitch.conf
pam.conf
pnm2ppa.conf
resolv.conf
rsyslog.conf
rygel.conf
sensors3.conf
sudo.conf
sudo_logsrvd.conf
sysctl.conf
ucf.conf
usb_modeswitch.conf
xattr.conf
brijesh@brijesh-Inspiron-5567:~$ 

```
### Question 14- Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
```
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ vim my_notes.txt
brijesh@brijesh-Inspiron-5567:~/Home/MyFiles$ 

Saturday 03 February 2024 08:58:36 PM IST
This is a new line of text.this is very important and i going to make it important.
                                                                        
::%s/critical/important/g   
```


### Question 15- Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.

```
brijesh@brijesh-Inspiron-5567:~$ # Create the user with the home directory
sudo useradd -m -d /home/john_doe -s /bin/bash john_doe

# Assign the user to the "users" group
sudo usermod -aG users john_doe
[sudo] password for brijesh: 
brijesh@brijesh-Inspiron-5567:~$ 

```

### Question 16- Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.
```

```
### Question 17- Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
```
brijesh@brijesh-Inspiron-5567:~$ sudo chsh -s /bin/bash john_doe
brijesh@brijesh-Inspiron-5567:~$ sudo chage -E $(date -d "+1 month" +%Y-%m-%d) john_doe
brijesh@brijesh-Inspiron-5567:~$ 

```

### Question 18- Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
```
brijesh@brijesh-Inspiron-5567:~$ sudo groupadd development_team
brijesh@brijesh-Inspiron-5567:~$ sudo usermod -aG development_team john_doe
brijesh@brijesh-Inspiron-5567:~$ getent group development_team
development_team:x:1002:john_doe
brijesh@brijesh-Inspiron-5567:~$ 
brijesh@brijesh-Inspiron-5567:~$ groups john_doe
john_doe : john_doe users development_team
brijesh@brijesh-Inspiron-5567:~$ 

```

### Question 19- Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.

```
brijesh@brijesh-Inspiron-5567:~$ sudo deluser john_doe users
Removing user `john_doe' from group `users' ...
Done.
brijesh@brijesh-Inspiron-5567:~$ sudo usermod -aG development_team john_doe
brijesh@brijesh-Inspiron-5567:~$ groups john_doe
john_doe : john_doe development_team
brijesh@brijesh-Inspiron-5567:~$ 

```

### Question 20- Delete the user account "john_doe" and ensure that their home directory is also removed.
```
brijesh@brijesh-Inspiron-5567:~$ sudo userdel -r john_doe
userdel: john_doe mail spool (/var/mail/john_doe) not found
brijesh@brijesh-Inspiron-5567:~$ 
```
### Question 21- Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
```h@brijesh-Inspiron-5567:~$ getent group development_team
development_team:x:1002:
brijesh@brijesh-Inspiron-5567:~$ for user in $(getent group development_team | cut -d: -f4 | tr ',' ' '); do
    sudo usermod -aG users $user
done
brijesh@brijesh-Inspiron-5567:~$ sudo groupdel development_team
brijesh@brijesh-Inspiron-5567:~$ 
```

### Question 22- Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.

```
brijesh@brijesh-Inspiron-5567:~$ sudo chage -M 90 -I -1 -m 0 -W 7 $(awk -F: '$3 >= 1000 && $1 != "nobody" {print $1}' /etc/passwd)
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS

brijesh@brijesh-Inspiron-5567:~$ sudo sed -i 's/PASS_MAX_DAYS.*/PASS_MAX_DAYS   90/' /etc/login.defs
brijesh@brijesh-Inspiron-5567:~$ 
```
### Question 23- Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.

```
brijesh@brijesh-Inspiron-5567:~$ sudo passwd -l john_doe
passwd: password expiry information changed.
brijesh@brijesh-Inspiron-5567:~$ su - john_doe
Password: 
su: Authentication failure
brijesh@brijesh-Inspiron-5567:~$ sudo passwd -u john_doe
passwd: password expiry information changed.
brijesh@brijesh-Inspiron-5567:~$ 
```
### Question 24- Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.

```
brijesh@brijesh-Inspiron-5567:~$ id john_doe
uid=1001(john_doe) gid=1001(john_doe) groups=1001(john_doe)
brijesh@brijesh-Inspiron-5567:~$ uid=1001(john_doe) gid=1001(john_doe) groups=1001(john_doe),1002(some_group),1003(another_group),...
bash: syntax error near unexpected token `('
brijesh@brijesh-Inspiron-5567:~$ 
```
### Question 25- Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.

```
brijesh@brijesh-Inspiron-5567:~$ sudo chage -M 60 john_doe
brijesh@brijesh-Inspiron-5567:~$ sudo chage -l john_doe
Last password change					: Feb 03, 2024
Password expires					: Apr 03, 2024
Password inactive					: never
Account expires						: never
Minimum number of days between password change		: 0
Maximum number of days between password change		: 60
Number of days of warning before password expires	: 7
brijesh@brijesh-Inspiron-5567:~$ 
```
