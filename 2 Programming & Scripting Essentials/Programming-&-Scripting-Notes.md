# Linux
- Open source OS
- Its robustness, security, and flexibility make it indispensable for data engineers.
- Known for flexibility, stability and security
  - customisable to specific needs
  - Supports and compatible with software tools and frameworks
  - Handles large datasets efficiently
## System sructure
![image](https://github.com/user-attachments/assets/ed6401a4-3883-4a60-95f6-991e12dc395f)

- Kernel - The core part of Linux that manages system resources, such as drivers and power usage
- Shell- The interface that allows users to interact with the kernel and with user programs/applications
- Applications - For example using the terminal to execute commands

## Filesystem hierarchy standard (FHS)
Govern the layout of Unix-like systems
https://www.coursera.org/articles/unix-vs-linux

### /bin
  - Binary files - contains essential binary executables that are required for the system to boot and run in single-user mode.
  - Provide essential commands and tools for both users and the system for basic operations
### /etc
  - Configuration files - contains all the system-wide configuration files and shell scripts that are used to boot and initialise system settings. This is where system administrators can configure the system's behaviour.
  - Store configuration files that dictate how the system and various services operate
### /home
  - Home directories - default location for users' personal directories. Each user on the system has a subdirectory within /home where their personal files, configurations, and documents are stored.
  - Provide a personal space for each user to store their files and settings, keeping them separate from system files and other users' data
### /usr
  - User Binaries & read only data
  - contains user utilities and applications that are not essential for the system to boot or operate in single-user mode. It is often considered the second major hierarchy and includes various subdirectories.
  - Subdirectories:
    - /usr/bin: Non-essential command binaries (like gcc, python)
    - /usr/lib: Libraries for binaries in /usr/bin and /usr/sbin
    - /usr/share: Architecture-independent data (like documentation, icons)
    - /usr/local: Locally installed software and custom scripts
    - Purpose: Store the majority of user-space applications and files, separating them from the root filesystem to facilitate easier management and maintenance.
### /var
  - Variable data
  - holds variable data files that are expected to grow in size over time. This includes system logs, user data files, caches, and other transient and dynamic files.
  - Store data that changes frequently, ensuring that the filesystem layout is organised and prevents / from being cluttered with variable data.

Navigation commands
![image](https://github.com/user-attachments/assets/3bafdaaa-dcfd-4b1e-9b21-4ec2fb2f176f)

## File Operations
Essential file operations include creating, deleting, moving, and copying files and directories.
https://dev.to/nadirbasalamah/file-operation-with-linux-command-31a9
touch - The touch command is used to create an empty file or update the timestamp of an existing file. 
  - eg. touch myfile.txt creates a new empty file. If the file exists, the timestamp will be set to current time/date
  - https://www.serveracademy.com/blog/how-to-use-the-touch-command-in-linux/#:~:text=The%20touch%20command%20is%20indispensable,%2Dc%20%2C%20and%20%2Dr%20.
rm - Remove files or Directories. Files are removed permanently
  - https://www.ionos.co.uk/digitalguide/server/configuration/linux-rm-command/
mv - move or rename files/directories 
cp - copy files/directories


pwd - Print working directory ie current path back to root
cd - change directory. cd Documents moves down to Documents file, cd / moves up to the next  level (cd .. is the same). cd ~ returns to the root
ls - lists information of current location
arguments
  - -l shows details about files
![image](https://github.com/user-attachments/assets/d1bbbad7-c789-48e5-903b-146edb966e17)
  - lt - sorts details by timestamp
  - -lS sort by file size
  - -r reverses sort order
![image](https://github.com/user-attachments/assets/62ae56f9-ae45-451f-b2a3-0a3f7068950b)


SuperUser
- su - password protected. Cursor chages from $ to #
- 'exit' to logoff
- sudo - use superuser access for one time execution. Password protected Can be used for other user accounts using -u
Changing permisiisions
chmod
![image](https://github.com/user-attachments/assets/f3e8e123-af29-4c15-b863-7e1b8c205cc1)
![image](https://github.com/user-attachments/assets/324eb596-bf8c-40ee-80e3-b6d40169e572)
changes user permission to executable on the hello.sh file

Execute a file - ./ filename


## Linux Utilities
### Global regular expression print (grep)
 - The primary function of grep is to search for and highlight specific text patterns within files.
- By using grep alongside utilities for sorting, counting, and aggregating data, we can track error frequencies and identify recurring issues.
- Commands: By using grep alongside utilities for sorting, counting, and aggregating data, they can track error frequencies and identify recurring issues.
- https://antonz.org/grep-by-example/
### Stream editor (sed)

### awk

## Job Scheduling & Automation

cron jobs are scheduled tasks that run at specified intervals

