# unix-commands
------------------
su: login as super user (e.g. root)
pwd: current directory
ls: list files
ls -l: list files with detail info
du -s [FOLDER_NAME]: folder size info
bunzip2 [FILE_NAME]: decompress file at same location
cp [FILE_1] [FILE_2]: copy file1 to a file called file2 
mv [FILE_1] [FILE_2] : (move) rename file1 to the name file2 
mv [FILE_1] /[FOLDER_NAME] : move file1 to the [FOLDER_NAME] directory 
df -k: disk size
df -g: disk size
ls -l | grep ^- | sort -nr -k 5 : order files as per size
rm * : deletes everything in a subdirectory (http://cmgm.stanford.edu/classes/unix/rm.html)
rm -r * : deletes everything in directory
rm test.txt : removes only file with a name "test.txt" on the end

rpm -ivh : install rpm bin file

/etc/init.d/chkconfig <SERVICE_NAME> off : off service at startup with super user (http://www.aboutlinux.info/2006/04/enabling-and-disabling-services-during_01.html)
/etc/init.d/chkconfig <SERVICE_NAME> on : start service at startup with super user (http://www.aboutlinux.info/2006/04/enabling-and-disabling-services-during_01.html)

tty : to check terminal
ps -ef | grep java : check the java processes 
kill -9 <process_id> : <process_id> is returned by prev command.

startx: start GUI
useradd <user>: create new user
passwd <user>: change password for user
groupadd <groupname>: create new group
usermod -g <groupname> <user>: Assign a user to a primary group
usermod -G <groupname> <user>: Assign a user to secondary groups
who am i : current user

vi [FILE_NAME]: edit file
dd : delete line
oo / o : insert new line after current line
OO / O : insert new line before curren line
[ESC] i ENTER : insert into file to location
[ESC]:wq! -> to file save
[ESC]:x -> to file save
cat [FILE_NAME]: view file
ifconfig: similar to ipconfig
/etc/init.d/network restart : restart network

vi ~/.bash_profile : env variable setup file
source ~/.bash_profile: export env variables to system
export JAVA_HOME=/root/java/jdk1.7.0_45
export MAVEN_HOME=/root/java/apache-maven-3.1.1
export ANT_HOME=/root/java/apache-ant-1.9.2
export PATH=$PATH:${JAVA_HOME}/bin:${MAVEN_HOME}/bin:${ANT_HOME}/bin

clear temp directory: http://forums.opensuse.org/english/get-technical-help-here/how-faq-forums/unreviewed-how-faq/412640-clear-temp-files-boot.html
sync; echo 3 > /proc/sys/vm/drop_caches : clear buffer cache

/tmp/VMwareDnD : VM ware DragNDrop files - verify and delete
------- increase swap size
dd if=/dev/zero of=/.swapfile bs=1M count=2048
mkswap -v1 /.swapfile
swapon /.swapfile
-------

ubuntu jdk setup : http://www.mkyong.com/java/how-to-install-java-jdk-on-ubuntu-linux/