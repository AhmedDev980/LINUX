1. Components of LINUX


 User Applications (Vim, Docker, Apache, etc.)     |
+----------------------------------------------------+
| Shell (Bash, Zsh, Fish, etc.)                     |  <-- Part of the OS
+----------------------------------------------------+
| System Libraries (glibc, libc, OpenSSL, etc.)     |  <-- Part of the OS
+----------------------------------------------------+
| System Utilities (ls, grep, systemctl, etc.)      |  <-- Part of the OS
+----------------------------------------------------+
| Linux Kernel (Process, Memory, FS, Network)       |  <-- Core of the OS
+----------------------------------------------------+
| Hardware (CPU, RAM, Disk, Network, Peripherals)   |
+----------------------------------------------------+

Shell (Command Line Interface - CLI)

🔹 A command interpreter that allows users to interact with the kernel.
🔹 Examples: Bash, Zsh, Fish, Dash, Ksh.
🔹 Converts user commands into system calls for the kernel.

# Linux distributions
1. ubuntu
2. centos
3. alpine
4. Debian

# command example
sudo apt install nginx
sudo - superuser (administrator). We need this to install software or make any system changes
apt - package manager
Install nginx - it will install nginx package

sudo apt update         # Update package lists
sudo apt upgrade -y     # Upgrade installed packages
sudo apt install nginx  # Install a package
sudo apt remove nginx   # Remove a package
sudo apt autoremove     # Remove unused dependencies
sudo apt search nginx   # Search for a package


addusr <username>  # To create user
ls /home # To check home dir is created for user
su - <username> # To login to user from root
sudo su - # To login to root
/etc/passwd # To check whether user is created or not
/etc/shadow # To check password is set or not


File and Directory Management
ls – Lists files and directories in the current location.
cd /path/to/directory – Changes the working directory.
pwd – Prints the current working directory.
mkdir new_folder – Creates a new directory.
rmdir empty_folder – Removes an empty directory.
rm file.txt – Deletes a file.
rm -r folder – Deletes a folder and its contents.
cp file1.txt file2.txt – Copies a file.
cp -r dir1 dir2 – Copies a directory recursively.
mv old_name new_name – Moves or renames a file or directory.

File Viewing and Editing
cat file.txt – Displays file content.
tac file.txt – Displays file content in reverse order.
less file.txt – Opens a file for viewing with scrolling support.
more file.txt – Similar to less, but only moves forward.
head -n 10 file.txt – Displays the first 10 lines of a file.
tail -n 10 file.txt – Displays the last 10 lines of a file.
nano file.txt – Opens a simple text editor.
vi file.txt – Opens a powerful text editor.
echo 'Hello' > file.txt – Writes text to a file, overwriting existing content.
echo 'Hello' >> file.txt – Appends text to a file without overwriting.

Basic Navigation
h – Move left
l – Move right
j – Move down
k – Move up
0 – Move to the beginning of the line
^ – Move to the first non-blank character of the line
$ – Move to the end of the line
w – Move to the next word
b – Move to the previous word
gg – Move to the start of the file
G – Move to the end of the file
:n – Move to line number n
Insert Mode Shortcuts
i – Insert before cursor
I – Insert at the beginning of the line
a – Append after cursor
A – Append at the end of the line
o – Open a new line below
O – Open a new line above
Esc – Exit insert mode
Editing Text
x – Delete a character
X – Delete a character before cursor
dw – Delete a word
dd – Delete a line
d$ – Delete from cursor to end of line
d0 – Delete from cursor to beginning of line
D – Delete from cursor to end of line
u – Undo last action
Ctrl + r – Redo an undone change
yy – Copy (yank) a line
yw – Copy (yank) a word
p – Paste after the cursor
P – Paste before the cursor
Search and Replace
/pattern – Search forward for a pattern
?pattern – Search backward for a pattern
n – Repeat last search forward
N – Repeat last search backward
:%s/old/new/g – Replace all occurrences of "old" with "new"
:s/old/new/g – Replace all occurrences in the current line
Working with Multiple Files
:e filename – Open a new file
:w – Save file
:wq – Save and exit
:q! – Quit without saving
:split filename – Split screen horizontally and open another file
:vsplit filename – Split screen vertically
Ctrl + w + w – Switch between split screens

ps aux # list processes
ps aux | grep java | grep -v grep # to ignore search word
kill <processid> # To kill process
kill -9 <processid> # To force kill
kill -3 <processid> # To get threadums or sub processes for java apps
kill -STOP <processid> # To stop process
kill -CONT <processid> # To continue or resume process
renice -n 5 -p <processid> # To make less priority
renice -n -10 -p <processid> # To make more priority
systemctl list-units --type=service # To list the service
systemctl stop <service name> # To stop service
systemctl start <service name> # To start service
Services start at the booting of server whereas process cant. Process can be converted to service.
CPU and Memory Monitoring
top – Real-time system monitoring
htop – Interactive process viewer (requires installation)
vmstat – Report system performance statistics
free -m – Show memory usage
Disk Monitoring
df -h – Check disk space usage
du -sh /path – Show disk usage of a specific directory
iostat – Display CPU and disk I/O statistics
lsblk # To list the disk. list blocks
