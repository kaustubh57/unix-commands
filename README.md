# UNIX commands

## Basic commands
- `su`: login as super user (e.g. root)
- `pwd`: current directory
- `ls`: list files
- `ls -l`: list files with detail info
- `bunzip2 [FILE_NAME]`: decompress file at same location
- `cp [FILE_1] [FILE_2]`: copy file1 to a file called file2 
- `mv [FILE_1] [FILE_2]`: (move) rename file1 to the name file2 
- `mv [FILE_1] /[FOLDER_NAME]`: move file1 to the [FOLDER_NAME] directory 
- `rm *`: deletes everything in a subdirectory (http://cmgm.stanford.edu/classes/unix/rm.html)
- `rm -r *`: deletes everything in directory
- `rm test.txt`: removes only file with a name "test.txt" on the end
- `tail -500 FILE_NAME | less`: see last 500 lines of files
- `cat [FILE_NAME]`: view file

## Size
- `df -k`: disk size
- `df -g`: disk size
- `df -h`: disk size
- `du -s [FOLDER_NAME]`: folder size info
- `du -sh ./`: current directory size
- `du -sh -- *(D) | sort -k1n`: order parent folder by size in ascending order
- `ls -l | grep ^- | sort -nr -k 5`: order files as per size

## Basic network commands
- `ifconfig`: similar to ipconfig (display network interface parameters)
- `hostname`: get machine's name
- `/etc/init.d/network restart`: restart network

## Install
- `rpm -ivh`: install rpm bin file

## Init file
- `/etc/init.d/chkconfig <SERVICE_NAME> off`: off service at startup with super user (http://www.aboutlinux.info/2006/04/enabling-and-disabling-services-during_01.html)
- `/etc/init.d/chkconfig <SERVICE_NAME> on`: start service at startup with super user (http://www.aboutlinux.info/2006/04/enabling-and-disabling-services-during_01.html)

## Terminal
- `tty`: to check terminal
- `ps -ef | grep java`: check the java processes 
- `kill -9 <process_id>`: <process_id> is returned by prev command.

## User
- `startx`: start GUI
- `useradd <user>`: create new user
- `passwd <user>`: change password for user
- `groupadd <groupname>`: create new group
- `usermod -g <groupname> <user>`: Assign a user to a primary group
- `usermod -G <groupname> <user>`: Assign a user to secondary groups
- `who am i`: current user

## vi Editor
- `vi [FILE_NAME]`: Open or edit a file.
- `Esc`: Switch to Command mode.
- `oo / o`: insert new line after current line
- `OO / O`: insert new line before curren line
- `i`: Switch to Insert mode.
- `[ESC] i ENTER`: insert into file to location
- `:w`: Save and continue editing
- `:wq` or `ZZ`: Save and quit/exit vi
- `:x`: to file save
- `:q!`: Quit vi and do not save changes
- `yy`: Yank (copy) a line of text
- `p`: Paste a line of yanked text below the current line
- `o`: Open a new line under the current line
- `O`: Open a new line above the current line
- `A`: Append to the end of the line
- `a`: Append after the cursor’s current position
- `I`: Insert text at the beginning of the current line
- `b`: Go to the beginning of the word
- `e`: Go to the end of the word
- `x`: Delete a single character
- `dd`: Delete an entire line
- `[X]dd`: Delete X number of lines
- `[X]yy`: Yank X number of lines
- `G`: Go to the last line in a file
- `[X]G`: Go to line X in a file
- `gg`: Go to the first line in a file
- `:num`: Display the current line’s line number
- `h`: Move left one character
- `l`: Move right one character
- `j`: Move down one line
- `k`: Move up one line

## Set ENV
- `vi ~/.bash_profile`: env variable setup file
- `source ~/.bash_profile`: export env variables to system
- `export JAVA_HOME=/root/java/jdk1.7.0_45`
- `export MAVEN_HOME=/root/java/apache-maven-3.1.1`
- `export ANT_HOME=/root/java/apache-ant-1.9.2`
- `export PATH=$PATH:${JAVA_HOME}/bin:${MAVEN_HOME}/bin:${ANT_HOME}/bin`

## Increase swap size
- `dd if=/dev/zero of=/.swapfile bs=1M count=2048`
- `mkswap -v1 /.swapfile`
- `swapon /.swapfile`

## Miscellaneous
- ubuntu jdk setup: http://www.mkyong.com/java/how-to-install-java-jdk-on-ubuntu-linux/
- clear temp directory: http://forums.opensuse.org/english/get-technical-help-here/how-faq-forums/unreviewed-how-faq/412640-clear-temp-files-boot.html
- `sync; echo 3 > /proc/sys/vm/drop_caches`: clear buffer cache
- `/tmp/VMwareDnD`: VM ware DragNDrop files - verify and delete
