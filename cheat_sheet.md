# Cheat Sheet

A list of useful commands that I will probably forget.

## Linux Commands

### SSH

`ssh <user>@<IP or Hostname>`  - Connect to remote machine

`wget <URL_to_file>` -  Download a file

### User Management

`useradd -c “Users Name” <username>` - Add new user

`groups <username>`	- List groups for user

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

### Kernel

`uname -r`	-Kernel version

`lsmod`	- List running kernel modules 

`depmod` -	Generate a list of kernel module dependencies and associated map files.

`insmod` -	Insert a module into the Linux kernel.

`modinfo` -	Show information about a Linux kernel module.

`modprobe` -	Add and remove modules from the Linux kernel.

`rmmod` -	Remove a module from the Linux kernel


### File System Management

`ls` -	List files and directories

`ls -l` -	With permissions shown

`cd`	

`mkdir <name>	`

`mkdir -m 700 <name>`	

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








