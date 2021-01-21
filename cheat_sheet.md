# Cheat Sheet

A list of useful commands that I will probably forget.

## Linux Commands

### SSH

`ssh <user>@<IP or Hostname>`  - Connect to remote machine

`wget <URL_to_file>` -  Download a file

### User Management

`sudo useradd -c “Users Name” <username>` - Add new user

`groups <username>`	- List groups for user

`whoami` - Shows user name

`sudo usermod -a -G <group> <username>` - Add user to group

`nano /etc/group` - Edit this file to remove users from groups 

### Networking

`ifconfig` - Show network configurations

`ping <address>`	- Ping a device

`traceroute <address>`	- Trace route to a device

### Run File

`source <filename>`	- Run given file

`. <filename>`	- Run given file

`source ~/.bashrc` - Run bash to undate current terminal session

### Environment Variables

`printenv` - Print all variables 

`set`	-

`unset` -	

`export`	- 


### Informational Commands

`ps` - Lists currently running process (programs).

`w` - Show who is logged on and what they are doing.

`id` - Print your user-id and group id's

`df` - Report filesystem disk space usage (“Disk Free” is how I remember it)

`du` - Disk Usage in a particular directory. “du -s” provides a summary for the current directory.

`top` - Displays CPU processes in a full-screen GUI. A great way to see the activity on your computer in real-time. Type “Q” to quit.

`free` - Displays the amount of free and used memory in the system.

`cat /proc/cpuinfo` - Displays information about your CPU.

`cat /proc/meminfo` - Display lots of information about current memory usage.

`uname -a` - Prints system information to the screen (kernel version, machine type, etc.)


### Kernel

`uname -r`	-Kernel version

`lsmod`	- List running kernel modules 

`depmod` -	Generate a list of kernel module dependencies and associated map files.

`insmod` -	Insert a module into the Linux kernel.

`modinfo` -	Show information about a Linux kernel module.

`modprobe` -	Add and remove modules from the Linux kernel.

`rmmod` -	Remove a module from the Linux kernel


### Pipe

`|`

`ls -l ~ | grep '^.....w'` - Chains commands together.


### Redirect

`ls -l *.py > pyfiles.txt` - Write output of command to file.

`ls -l *.py >> pyfiles.txt`- Append output of command to file.

### GREP

`grep`

`egrep`

### Disk Managemennt

`mount` - Show all mounted 

`mount -t ext4` - Only show ext4

`sudo mount /dev/sdb1 /mnt/media` = 

### File System Management

`which <Command>` - Shows the full path of shell commands found in your path

`whereis <Command>` - Locates the program, source code, and manual page for a command

`find` - Search for files matching certain patterns

`pwd` - Print working directory

`ls` -	List files and directories

`ls -l` -	With permissions shown

`cd`	

`mkdir [-p] <dirname>` - Make directory where -p creates parents.

`mkdir -m 700 <dirname>`	

`rmdir <dirname>`

`rm -rf directory` - Recursively -r removes the directory and all files and directories in that directory structure. Use with caution. There is no "trash" container to quickly 
restore your file from when using the command line. When you delete something, it is gone.


`chmod 777 filename` 	

0 – no permission
1 – execute
2 – write
3 – write and execute
4 – read
5 – read and execute
6 – read and write
7 – read, write, and execute
First Owner,  second digit is Group and the third digit is Others

### Package Management

`sudo apt update`	Update list of available packages
`sudo apt upgrade`	Upgrade packages
`sudo apt full-upgrade`	
`sudo apt update && sudo apt upgrade -y`	Quick update and upgrade command
`sudo apt install <package_name>`	Install
`sudo apt install <package_name>=<version_number>`	Install specific version of package
`sudo apt remove <package_name>`	
`sudo apt autoremove` 	
`sudo apt purge <package_name>`	
`apt search <search_term>`	
`apt show <package _term>`	
`apt list –-upgradable`	
`apt list –-installed`	
`apt list –-all-versions`	
`sudo dpkg -i <filename>.deb`	Install a downloaded DEB file

### CUDA 

`nvcc --version` - Get CUDA version

`/usr/local/cuda/bin/nvcc --version`	

### CONDA

`conda create -n myenv python=3.6` - Create with specifc Python version

`conda activate <ENVNAME>`

'conda install <PACKAGE>`

### GIT

`git config --global user.name “[firstname lastname]”` - set a name that is identifiable for credit when review version history

`git config --global user.email “[valid-email]”` - set an email address that will be associated with each history marker

`git config --global color.ui auto` - set automatic command line coloring for Git for easy reviewing

`git init` - initialize an existing directory as a Git repository

`git clone <url>` - retrieve an entire repository from a hosted location via URL

`git status` - 

`git add <file>`  - Add file use * for all.

`git commit -m "Commit Message"`








