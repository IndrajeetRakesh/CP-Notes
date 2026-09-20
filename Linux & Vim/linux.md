# Linux Terminal Commands

## 1. Basic Navigation

### `pwd`

**Work:** Shows the current working directory.

**Syntax:**

```bash
pwd
```

**Example:**

```bash
pwd
```

**Output:**

```text
/home/siddhant
```

---

### `ls`

**Work:** Shows files and folders in the current directory.

**Syntax:**

```bash
ls
```

**Example:**

```bash
ls
```

---

### `ls -l`

**Work:** Shows files and folders with detailed information.

**Syntax:**

```bash
ls -l
```

**Example:**

```bash
ls -l
```

---

### `ls -a`

**Work:** Shows all files and folders, including hidden files.

**Syntax:**

```bash
ls -a
```

**Example:**

```bash
ls -a
```

---

### `ls -la`

**Work:** Shows all files, including hidden files, with detailed information.

**Syntax:**

```bash
ls -la
```

**Example:**

```bash
ls -la
```

---

### `cd`

**Work:** Changes the current directory.

**Syntax:**

```bash
cd directory_name
```

**Example:**

```bash
cd Documents
```

---

### `cd ..`

**Work:** Moves one directory back/up.

**Syntax:**

```bash
cd ..
```

**Example:**

```bash
cd ..
```

---

### `cd ~`

**Work:** Goes to the home directory.

**Syntax:**

```bash
cd ~
```

**Example:**

```bash
cd ~
```

---

### `cd /`

**Work:** Goes to the root directory.

**Syntax:**

```bash
cd /
```

**Example:**

```bash
cd /
```

---

### `cd -`

**Work:** Goes back to the previous directory.

**Syntax:**

```bash
cd -
```

**Example:**

```bash
cd -
```

---

# 2. File and Directory Commands

## `mkdir`

**Work:** Creates a new directory.

**Syntax:**

```bash
mkdir directory_name
```

**Example:**

```bash
mkdir projects
```

---

### `mkdir -p`

**Work:** Creates parent directories if they don't already exist.

**Syntax:**

```bash
mkdir -p parent/child
```

**Example:**

```bash
mkdir -p projects/java/notes
```

---

### `touch`

**Work:** Creates an empty file.

**Syntax:**

```bash
touch filename
```

**Example:**

```bash
touch notes.txt
```

---

### `cp`

**Work:** Copies a file or directory.

**Syntax:**

```bash
cp source destination
```

**Example:**

```bash
cp notes.txt backup.txt
```

---

### `cp -r`

**Work:** Copies a directory and everything inside it.

**Syntax:**

```bash
cp -r source_directory destination_directory
```

**Example:**

```bash
cp -r projects projects_backup
```

---

### `mv`

**Work:** Moves a file/directory or renames it.

**Syntax:**

```bash
mv source destination
```

**Example — Move:**

```bash
mv notes.txt Documents/
```

**Example — Rename:**

```bash
mv old.txt new.txt
```

---

### `rm`

**Work:** Deletes a file.

**Syntax:**

```bash
rm filename
```

**Example:**

```bash
rm notes.txt
```

---

### `rm -r`

**Work:** Deletes a directory and everything inside it.

**Syntax:**

```bash
rm -r directory
```

**Example:**

```bash
rm -r projects
```

---

### `rm -f`

**Work:** Forcefully deletes a file without asking for confirmation.

**Syntax:**

```bash
rm -f filename
```

**Example:**

```bash
rm -f notes.txt
```

---

### `rm -rf`

**Work:** Forcefully deletes a directory and all its contents.

**Syntax:**

```bash
rm -rf directory
```

**Example:**

```bash
rm -rf projects
```

---

### `rmdir`

**Work:** Removes an empty directory.

**Syntax:**

```bash
rmdir directory
```

**Example:**

```bash
rmdir empty_folder
```

---

# 3. File Content Commands

## `cat`

**Work:** Displays the contents of a file.

**Syntax:**

```bash
cat filename
```

**Example:**

```bash
cat notes.txt
```

---

### `cat -n`

**Work:** Displays file contents with line numbers.

**Syntax:**

```bash
cat -n filename
```

**Example:**

```bash
cat -n notes.txt
```

---

### `less`

**Work:** Opens a file for viewing one screen at a time.

**Syntax:**

```bash
less filename
```

**Example:**

```bash
less notes.txt
```

Press `q` to exit.

---

### `more`

**Work:** Displays a file one screen at a time.

**Syntax:**

```bash
more filename
```

**Example:**

```bash
more notes.txt
```

---

### `head`

**Work:** Shows the first 10 lines of a file.

**Syntax:**

```bash
head filename
```

**Example:**

```bash
head notes.txt
```

---

### `head -n`

**Work:** Shows a specific number of lines from the beginning.

**Syntax:**

```bash
head -n number filename
```

**Example:**

```bash
head -n 5 notes.txt
```

---

### `tail`

**Work:** Shows the last 10 lines of a file.

**Syntax:**

```bash
tail filename
```

**Example:**

```bash
tail notes.txt
```

---

### `tail -n`

**Work:** Shows a specific number of lines from the end.

**Syntax:**

```bash
tail -n number filename
```

**Example:**

```bash
tail -n 5 notes.txt
```

---

### `tail -f`

**Work:** Continuously displays new content added to a file.

**Syntax:**

```bash
tail -f filename
```

**Example:**

```bash
tail -f server.log
```

Press `Ctrl + C` to stop.

---

# 4. Creating and Editing Files

## `echo`

**Work:** Prints text in the terminal.

**Syntax:**

```bash
echo "text"
```

**Example:**

```bash
echo "Hello World"
```

---

### `echo >`

**Work:** Writes text to a file and replaces existing content.

**Syntax:**

```bash
echo "text" > filename
```

**Example:**

```bash
echo "Hello" > notes.txt
```

---

### `echo >>`

**Work:** Adds text to the end of a file.

**Syntax:**

```bash
echo "text" >> filename
```

**Example:**

```bash
echo "World" >> notes.txt
```

---

### `nano`

**Work:** Opens a simple terminal text editor.

**Syntax:**

```bash
nano filename
```

**Example:**

```bash
nano notes.txt
```

---

### `vim`

**Work:** Opens the Vim text editor.

**Syntax:**

```bash
vim filename
```

**Example:**

```bash
vim notes.txt
```

---

# 5. Searching Commands

## `grep`

**Work:** Searches for text inside files.

**Syntax:**

```bash
grep "text" filename
```

**Example:**

```bash
grep "Java" notes.txt
```

---

### `grep -i`

**Work:** Searches without considering uppercase/lowercase.

**Syntax:**

```bash
grep -i "text" filename
```

**Example:**

```bash
grep -i "java" notes.txt
```

---

### `grep -n`

**Work:** Shows the line number where the matching text occurs.

**Syntax:**

```bash
grep -n "text" filename
```

**Example:**

```bash
grep -n "Java" notes.txt
```

---

### `grep -r`

**Work:** Searches recursively inside directories.

**Syntax:**

```bash
grep -r "text" directory
```

**Example:**

```bash
grep -r "Java" projects/
```

---

### `find`

**Work:** Searches for files and directories.

**Syntax:**

```bash
find location -name "filename"
```

**Example:**

```bash
find . -name "notes.txt"
```

---

### `find -type f`

**Work:** Searches only for files.

**Syntax:**

```bash
find location -type f
```

**Example:**

```bash
find . -type f
```

---

### `find -type d`

**Work:** Searches only for directories.

**Syntax:**

```bash
find location -type d
```

**Example:**

```bash
find . -type d
```

---

# 6. File Information

## `file`

**Work:** Shows the type of a file.

**Syntax:**

```bash
file filename
```

**Example:**

```bash
file notes.txt
```

---

### `wc`

**Work:** Counts lines, words, and characters/bytes.

**Syntax:**

```bash
wc filename
```

**Example:**

```bash
wc notes.txt
```

---

### `wc -l`

**Work:** Counts lines.

**Syntax:**

```bash
wc -l filename
```

**Example:**

```bash
wc -l notes.txt
```

---

### `wc -w`

**Work:** Counts words.

**Syntax:**

```bash
wc -w filename
```

**Example:**

```bash
wc -w notes.txt
```

---

### `wc -c`

**Work:** Counts bytes.

**Syntax:**

```bash
wc -c filename
```

**Example:**

```bash
wc -c notes.txt
```

---

### `du`

**Work:** Shows disk space used by files/directories.

**Syntax:**

```bash
du
```

**Example:**

```bash
du
```

---

### `du -h`

**Work:** Shows disk usage in human-readable format.

**Syntax:**

```bash
du -h
```

**Example:**

```bash
du -h projects/
```

---

### `df`

**Work:** Shows available and used disk space.

**Syntax:**

```bash
df
```

**Example:**

```bash
df
```

---

### `df -h`

**Work:** Shows disk space in human-readable format.

**Syntax:**

```bash
df -h
```

**Example:**

```bash
df -h
```

---

# 7. Permissions

## `ls -l`

**Work:** Shows file permissions.

**Example:**

```bash
ls -l
```

Example output:

```text
-rwxr-xr-- 1 user user 1200 notes.txt
```

Permission groups:

```text
-rwxr-xr--
 │││ │││ │││
 │││ │││ └── Others
 │││ └────── Group
 └────────── Owner
```

---

## Permission Types

```text
r = read
w = write
x = execute
```

Values:

```text
r = 4
w = 2
x = 1
```

Examples:

```text
rwx = 7
rw- = 6
r-x = 5
r-- = 4
```

---

## `chmod`

**Work:** Changes file or directory permissions.

**Syntax:**

```bash
chmod permissions filename
```

**Example:**

```bash
chmod 755 script.sh
```

---

### `chmod +x`

**Work:** Adds execute permission.

**Syntax:**

```bash
chmod +x filename
```

**Example:**

```bash
chmod +x script.sh
```

---

### `chmod -x`

**Work:** Removes execute permission.

**Syntax:**

```bash
chmod -x filename
```

**Example:**

```bash
chmod -x script.sh
```

---

### `chmod u+x`

**Work:** Gives execute permission to the owner.

**Syntax:**

```bash
chmod u+x filename
```

**Example:**

```bash
chmod u+x script.sh
```

---

### `chmod g+w`

**Work:** Gives write permission to the group.

**Syntax:**

```bash
chmod g+w filename
```

**Example:**

```bash
chmod g+w notes.txt
```

---

### `chmod o-r`

**Work:** Removes read permission from others.

**Syntax:**

```bash
chmod o-r filename
```

**Example:**

```bash
chmod o-r notes.txt
```

---

## Permission Numbers

### `chmod 777`

```bash
chmod 777 file
```

Meaning:

```text
Owner  = rwx
Group  = rwx
Others = rwx
```

---

### `chmod 755`

```bash
chmod 755 script.sh
```

Meaning:

```text
Owner  = rwx
Group  = r-x
Others = r-x
```

---

### `chmod 644`

```bash
chmod 644 notes.txt
```

Meaning:

```text
Owner  = rw-
Group  = r--
Others = r--
```

---

# 8. Ownership

## `chown`

**Work:** Changes file owner.

**Syntax:**

```bash
chown user filename
```

**Example:**

```bash
sudo chown siddhant notes.txt
```

---

### `chgrp`

**Work:** Changes the group ownership.

**Syntax:**

```bash
chgrp group filename
```

**Example:**

```bash
sudo chgrp students notes.txt
```

---

# 9. System Information

## `whoami`

**Work:** Shows the current username.

```bash
whoami
```

---

### `id`

**Work:** Shows user ID and group information.

```bash
id
```

---

### `uname`

**Work:** Shows system information.

```bash
uname
```

---

### `uname -a`

**Work:** Shows detailed system information.

```bash
uname -a
```

---

### `hostname`

**Work:** Shows the computer's hostname.

```bash
hostname
```

---

### `date`

**Work:** Shows the current date and time.

```bash
date
```

---

### `cal`

**Work:** Shows a calendar.

```bash
cal
```

---

### `uptime`

**Work:** Shows how long the system has been running.

```bash
uptime
```

---

# 10. Process Management

## `ps`

**Work:** Shows running processes.

```bash
ps
```

---

### `ps aux`

**Work:** Shows detailed information about running processes.

```bash
ps aux
```

---

### `top`

**Work:** Shows running processes and system resource usage in real time.

```bash
top
```

Press:

```text
q
```

to exit.

---

### `kill`

**Work:** Stops a process using its process ID.

**Syntax:**

```bash
kill PID
```

**Example:**

```bash
kill 1234
```

---

### `kill -9`

**Work:** Forcefully terminates a process.

**Syntax:**

```bash
kill -9 PID
```

**Example:**

```bash
kill -9 1234
```

---

### `jobs`

**Work:** Shows jobs running in the current terminal.

```bash
jobs
```

---

### `fg`

**Work:** Brings a background job to the foreground.

```bash
fg
```

---

### `bg`

**Work:** Continues a stopped job in the background.

```bash
bg
```

---

# 11. Terminal Control

## `clear`

**Work:** Clears the terminal screen.

```bash
clear
```

---

### `history`

**Work:** Shows previously executed commands.

```bash
history
```

---

### `!!`

**Work:** Runs the previous command again.

```bash
!!
```

---

### `Ctrl + C`

Stops the currently running command.

---

### `Ctrl + D`

Exits the current shell/session.

---

### `Ctrl + L`

Clears the terminal screen.

---

### `Ctrl + Z`

Suspends the currently running process.

---

# 12. Redirection

## `>`

**Work:** Sends output to a file and replaces existing content.

```bash
echo "Hello" > notes.txt
```

---

## `>>`

**Work:** Adds output to the end of a file.

```bash
echo "World" >> notes.txt
```

---

## `<`

**Work:** Takes input from a file.

```bash
command < file
```

Example:

```bash
sort < names.txt
```

---

## `2>`

**Work:** Redirects error messages to a file.

```bash
command 2> error.txt
```

Example:

```bash
ls unknown 2> error.txt
```

---

## `&>`

**Work:** Redirects both normal output and errors.

```bash
command &> output.txt
```

Example:

```bash
ls /home &> output.txt
```

---

# 13. Pipes

## `|`

**Work:** Sends the output of one command as input to another command.

**Syntax:**

```bash
command1 | command2
```

**Example:**

```bash
ls | grep ".txt"
```

Another example:

```bash
cat notes.txt | grep "Java"
```

---

### Multiple Pipes

```bash
cat notes.txt | grep "Java" | wc -l
```

This:

1. Reads the file
2. Finds lines containing `Java`
3. Counts those lines

---

# 14. Sorting

## `sort`

**Work:** Sorts lines alphabetically.

```bash
sort names.txt
```

---

### `sort -r`

**Work:** Sorts in reverse order.

```bash
sort -r names.txt
```

---

### `sort -n`

**Work:** Sorts numbers numerically.

```bash
sort -n numbers.txt
```

---

### `sort -u`

**Work:** Sorts and removes duplicate lines.

```bash
sort -u names.txt
```

---

# 15. `uniq`

## `uniq`

**Work:** Removes adjacent duplicate lines.

```bash
uniq names.txt
```

Usually used with `sort`:

```bash
sort names.txt | uniq
```

---

### `uniq -c`

**Work:** Counts repeated lines.

```bash
sort names.txt | uniq -c
```

---

# 16. `cut`

## `cut`

**Work:** Extracts parts of each line.

### Extract characters

```bash
cut -c 1-5 file.txt
```

Shows characters 1 to 5.

---

### Extract columns

```bash
cut -d "," -f 1 data.csv
```

Here:

```text
-d "," → delimiter is comma
-f 1   → select first field
```

---

# 17. `tr`

## `tr`

**Work:** Translates or replaces characters.

```bash
echo "hello" | tr 'a-z' 'A-Z'
```

Output:

```text
HELLO
```

---

### Replace characters

```bash
echo "hello" | tr 'e' 'a'
```

Output:

```text
hallo
```

---

# 18. `sed`

## `sed`

**Work:** Searches and modifies text.

### Replace text

```bash
sed 's/old/new/' file.txt
```

Example:

```bash
sed 's/Java/Python/' notes.txt
```

---

### Replace all occurrences on each line

```bash
sed 's/Java/Python/g' notes.txt
```

---

# 19. `awk`

## `awk`

**Work:** Processes and extracts columns from text.

```bash
awk '{print $1}' file.txt
```

Shows the first column.

---

Example:

```bash
echo "Siddhant 20" | awk '{print $1}'
```

Output:

```text
Siddhant
```

---

# 20. Archives and Compression

## `tar`

**Work:** Creates or extracts archive files.

### Create archive

```bash
tar -cf files.tar files/
```

---

### Extract archive

```bash
tar -xf files.tar
```

---

### Create `.tar.gz`

```bash
tar -czf files.tar.gz files/
```

---

### Extract `.tar.gz`

```bash
tar -xzf files.tar.gz
```

---

## `gzip`

**Work:** Compresses a file.

```bash
gzip file.txt
```

---

## `gunzip`

**Work:** Extracts a `.gz` file.

```bash
gunzip file.txt.gz
```

---

# 21. Networking

## `ip`

**Work:** Shows and manages network information.

```bash
ip addr
```

---

### `ip route`

**Work:** Shows routing information.

```bash
ip route
```

---

## `ping`

**Work:** Checks whether a host is reachable.

```bash
ping google.com
```

Stop with:

```text
Ctrl + C
```

---

## `curl`

**Work:** Transfers data from or to a URL.

```bash
curl https://example.com
```

---

## `wget`

**Work:** Downloads files from the internet.

```bash
wget https://example.com/file.zip
```

---

## `ssh`

**Work:** Connects to another computer securely through SSH.

```bash
ssh username@hostname
```

Example:

```bash
ssh user@192.168.1.10
```

---

## `scp`

**Work:** Copies files between computers using SSH.

```bash
scp file.txt user@server:/home/user/
```

---

# 22. Package Management — Ubuntu/Debian

## `apt update`

**Work:** Updates the package information.

```bash
sudo apt update
```

---

## `apt upgrade`

**Work:** Upgrades installed packages.

```bash
sudo apt upgrade
```

---

## `apt install`

**Work:** Installs a package.

```bash
sudo apt install package-name
```

Example:

```bash
sudo apt install git
```

---

## `apt remove`

**Work:** Removes a package.

```bash
sudo apt remove package-name
```

Example:

```bash
sudo apt remove nano
```

---

## `apt search`

**Work:** Searches for packages.

```bash
apt search package-name
```

Example:

```bash
apt search python
```

---

## `apt show`

**Work:** Shows information about a package.

```bash
apt show package-name
```

Example:

```bash
apt show git
```

---

# 23. `sudo`

## `sudo`

**Work:** Runs a command with administrator privileges.

**Syntax:**

```bash
sudo command
```

**Example:**

```bash
sudo apt update
```

---

# 24. Environment Variables

## `env`

**Work:** Shows environment variables.

```bash
env
```

---

## `printenv`

**Work:** Displays environment variables.

```bash
printenv
```

---

## `echo $PATH`

**Work:** Shows the directories where Linux searches for commands.

```bash
echo $PATH
```

---

## `export`

**Work:** Creates or modifies an environment variable.

```bash
export NAME="Siddhant"
```

Check it:

```bash
echo $NAME
```

---

# 25. Shell Information

## `which`

**Work:** Shows the location of a command.

```bash
which python
```

Example output:

```text
/usr/bin/python
```

---

## `whereis`

**Work:** Finds the binary, source, and manual locations of a command.

```bash
whereis python
```

---

## `type`

**Work:** Shows what type of command something is.

```bash
type ls
```

---

## `alias`

**Work:** Creates shortcuts for commands.

```bash
alias ll='ls -la'
```

Then:

```bash
ll
```

---

## `unalias`

**Work:** Removes an alias.

```bash
unalias ll
```

---

# 26. Manual / Help

## `man`

**Work:** Opens the manual page for a command.

**Syntax:**

```bash
man command
```

**Example:**

```bash
man ls
```

Exit:

```text
q
```

---

## `command --help`

**Work:** Shows basic help for a command.

```bash
ls --help
```

Example:

```bash
grep --help
```

---

## `info`

**Work:** Shows detailed documentation.

```bash
info ls
```

---

# 27. Links

## `ln`

**Work:** Creates a hard link.

```bash
ln file.txt link.txt
```

---

## `ln -s`

**Work:** Creates a symbolic/soft link.

```bash
ln -s file.txt link.txt
```

---

# 28. Disk and Memory

## `free`

**Work:** Shows RAM and swap memory usage.

```bash
free
```

---

### `free -h`

**Work:** Shows memory in human-readable format.

```bash
free -h
```

---

## `lsblk`

**Work:** Shows storage devices and partitions.

```bash
lsblk
```

---

## `mount`

**Work:** Shows mounted filesystems or mounts a filesystem.

```bash
mount
```

---

## `umount`

**Work:** Unmounts a filesystem.

```bash
sudo umount /mount/point
```

---

# 29. User Management

## `who`

**Work:** Shows currently logged-in users.

```bash
who
```

---

## `w`

**Work:** Shows logged-in users and what they are doing.

```bash
w
```

---

## `passwd`

**Work:** Changes the user's password.

```bash
passwd
```

---

## `su`

**Work:** Switches to another user.

```bash
su username
```

---

# 30. Process and Job Commands

## Run in Background

```bash
command &
```

Example:

```bash
gedit &
```

---

## `jobs`

```bash
jobs
```

Shows background/stopped jobs.

---

## `fg`

```bash
fg
```

Brings a background job to the foreground.

---

## `bg`

```bash
bg
```

Runs a stopped job in the background.

---

# 31. Date and Time

## `date`

```bash
date
```

Shows current date and time.

---

### Custom date format

```bash
date +"%Y-%m-%d"
```

Example output:

```text
2026-09-20
```

---

# 32. Useful Text Commands

## `printf`

**Work:** Prints formatted text.

```bash
printf "Hello %s\n" "Siddhant"
```

---

## `rev`

**Work:** Reverses text.

```bash
echo "hello" | rev
```

Output:

```text
olleh
```

---

## `seq`

**Work:** Generates a sequence of numbers.

```bash
seq 1 5
```

Output:

```text
1
2
3
4
5
```

---

# 33. Command History

## `history`

```bash
history
```

---

### Search history

```bash
history | grep git
```

Shows previous commands containing `git`.

---

# 34. Wildcards

## `*`

**Work:** Matches any number of characters.

```bash
ls *.txt
```

Shows all `.txt` files.

---

## `?`

**Work:** Matches exactly one character.

```bash
ls file?.txt
```

Matches:

```text
file1.txt
file2.txt
```

---

## `[]`

**Work:** Matches one character from a set/range.

```bash
ls file[123].txt
```

Matches:

```text
file1.txt
file2.txt
file3.txt
```

---

# 35. Special Symbols

| Symbol | Meaning                               | Example                 |                                    |          |   |             |
| ------ | ------------------------------------- | ----------------------- | ---------------------------------- | -------- | - | ----------- |
| `.`    | Current directory                     | `./file`                |                                    |          |   |             |
| `..`   | Parent directory                      | `cd ..`                 |                                    |          |   |             |
| `~`    | Home directory                        | `cd ~`                  |                                    |          |   |             |
| `/`    | Root directory/path separator         | `cd /`                  |                                    |          |   |             |
| `*`    | Any number of characters              | `ls *.txt`              |                                    |          |   |             |
| `?`    | One character                         | `file?.txt`             |                                    |          |   |             |
| `      | `                                     | Pipe                    | `ls \| grep txt`                   |          |   |             |
| `>`    | Redirect/overwrite                    | `echo hi > file`        |                                    |          |   |             |
| `>>`   | Redirect/append                       | `echo hi >> file`       |                                    |          |   |             |
| `<`    | Input redirection                     | `sort < file`           |                                    |          |   |             |
| `&`    | Run in background                     | `command &`             |                                    |          |   |             |
| `&&`   | Run next command if previous succeeds | `mkdir test && cd test` |                                    |          |   |             |
| `      |                                       | `                       | Run next command if previous fails | `cd test |   | mkdir test` |
| `;`    | Run commands sequentially             | `pwd; ls`               |                                    |          |   |             |

---

# 36. Command Chaining

## `&&`

Runs the second command only if the first command succeeds.

```bash
mkdir test && cd test
```

---

## `||`

Runs the second command only if the first command fails.

```bash
cd test || mkdir test
```

---

## `;`

Runs commands one after another regardless of success/failure.

```bash
pwd; ls; date
```

---

# 37. Important Linux File Types

You can see file types using:

```bash
ls -l
```

Common symbols:

```text
-   Regular file
d   Directory
l   Symbolic link
c   Character device
b   Block device
p   Named pipe
s   Socket
```

Example:

```text
-rw-r--r--  notes.txt
drwxr-xr-x  projects
lrwxrwxrwx  shortcut
```

---

# 38. Important Commands for ICP

These are the commands you should know especially well:

```bash
pwd
ls
ls -l
ls -a
ls -la
cd
cd ..
cd ~
mkdir
mkdir -p
touch
cp
cp -r
mv
rm
rm -r
rmdir
cat
cat -n
head
head -n
tail
tail -n
grep
grep -i
grep -n
grep -r
find
wc
sort
uniq
cut
tr
sed
awk
echo
chmod
chmod +x
chmod 755
chmod 644
chown
ps
ps aux
top
kill
jobs
fg
bg
clear
history
man
which
whoami
id
uname
df
du
free
ip
ping
curl
sudo
apt
```

# 39. Most Important Syntax Patterns

```bash
command
```

```bash
command argument
```

```bash
command -option
```

```bash
command -option argument
```

```bash
command1 | command2
```

```bash
command > file
```

```bash
command >> file
```

```bash
command < file
```

```bash
command1 && command2
```

```bash
command1 || command2
```

```bash
command &
```

# 40. Quick Revision Table

| Command   | Work                       |
| --------- | -------------------------- |
| `pwd`     | Current directory          |
| `ls`      | List files                 |
| `cd`      | Change directory           |
| `mkdir`   | Create directory           |
| `touch`   | Create file                |
| `cp`      | Copy                       |
| `mv`      | Move/rename                |
| `rm`      | Delete                     |
| `rmdir`   | Delete empty directory     |
| `cat`     | Display file               |
| `head`    | First lines                |
| `tail`    | Last lines                 |
| `grep`    | Search text                |
| `find`    | Find files/directories     |
| `wc`      | Count lines/words/bytes    |
| `sort`    | Sort text                  |
| `uniq`    | Remove/count duplicates    |
| `cut`     | Extract columns/characters |
| `tr`      | Translate characters       |
| `sed`     | Edit/replace text          |
| `awk`     | Process text/columns       |
| `chmod`   | Change permissions         |
| `chown`   | Change owner               |
| `ps`      | Show processes             |
| `top`     | Monitor processes          |
| `kill`    | Stop process               |
| `df`      | Disk space                 |
| `du`      | Directory/file space       |
| `free`    | RAM usage                  |
| `ip`      | Network information        |
| `ping`    | Test connection            |
| `curl`    | Transfer/request data      |
| `wget`    | Download files             |
| `sudo`    | Administrator command      |
| `apt`     | Package management         |
| `man`     | Manual                     |
| `history` | Command history            |
| `clear`   | Clear terminal             |
| `whoami`  | Current user               |
| `uname`   | System information         |
| `which`   | Command location           |
| `tar`     | Archive/extract            |
| `gzip`    | Compress                   |
| `ssh`     | Remote connection          |
| `scp`     | Secure file copy           |
