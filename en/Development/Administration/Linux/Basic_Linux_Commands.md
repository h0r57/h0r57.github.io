Basic Linux Commands
====================

System
------

| Command            | Description                                       |
| :----------------- | :------------------------------------------------ |
| shutdown -h now    | Shut down machine now                             |
| reboot             | Restart machine                                   |
| date               | Show the current date and time                    |
| whoami             | Who you are logged in as                          |
| finger user        | Display information about user                    |
| man command        | Show the manual for command                       |
| df -T -h           | Show disk usage with type and human readable size |
| du                 | Show directory space usage                        |
| free               | Show memory and swap usage                        |
| which app          | Show location of app                              |
| uname -a           | Show system information                           |
| passwd user        |                                                   |
| ifconfig -a        |                                                   |
| ifconfig eth0 up   |                                                   |
| ifconfig eth0 down |                                                   |
| whatis app         |                                                   |
| su - user          |                                                   |
| clear              |                                                   |


Process Management
------------------

| Command                | Description                             |
| :-----------------     | :-------------------------------------- |
| top                    | Display all running processes           |
| ps -ef                 | Display your currently active processes |
| ps -ef &#124; grep vim | Display a specific process              |
| kill pid               | Kill process id pid                     |
| kill -9 pid            | Force kill process id pid               |


Packet Manager
--------------

| Command              | Description                    |
| :------------------- | :----------------------------- |
| yum install httpd    |                                |
| yum update httpd     |                                |
| yum remove httpd     |                                |
| rpm -ivh httpd-*.rpm |                                |
| rpm -ivh httpd-*.rpm |                                |
| rpm -ivh httpd-*.rpm |                                |
| apt update           |                                |
| apt install httpd    |                                |
| apt upgrade          |                                |
| apt remove httpd     |                                |
| apt purge httpd      |                                |
| dpkg -i httpd-*.deb  |                                |
| dpkg -r httpd-*.deb  |                                |
| dpkg -P httpd-*.deb  |                                |


History
-------

| Command           | Description                                                                                                   |
| :---------------- | :------------------------------------------------------------------------------------------------------------ |
| vmstat            |                                                                                                               |
| history 10        |                                                                                                               |
| !40               |                                                                                                               |
| !!                |                                                                                                               |
| sudo !!           |                                                                                                               |
| !apt              |                                                                                                               |
| last              | History of last logged in users                                                                               |
| <space>command    | Prevent a command from being recorded in history using a space prefix                                         |
| <alt>. And <esc>. | A tweak which put the last command argument at prompt, in the order of last entered command, appearing first. |


Calculations
------------

| Command     | Description                                         |
| :---------- | :-------------------------------------------------- |
| expr 2 + 3  |                                                     |
| expr 6 – 3  |                                                     |
| expr 12 / 3 |                                                     |
| expr 2 \* 9 |                                                     |
| factor      | Gives all the possible factors of a decimal number. |


File System
-----------

| Command                                  | Description                                                                |
| :--------------------------------        | :------------------------------------------------------------------------- |
| pwd                                      | Show path of current directory                                             |
| cd                                       | Change directory to your home directory                                    |
| cd ..                                    | Change directory up one directory                                          |
| cd /                                     | Change directory to the root directory                                     |
| cd -                                     | Go back to the last directory                                              |
| cd dir                                   | Change directory to dir                                                    |
| ls dir                                   | List all items in directory dir                                            |
| ls                                       | List items in the current directory                                        |
| ls -lh                                   | List items with perimissions, size (human readable), and modification date |
| ls -a                                    | List all items in current directory, including hidden files                |
| mkdir dir                                | Make directory dir                                                         |
| rm file                                  | Remove file                                                                |
| rm -r dir                                | Remove directory dir recursively                                           |
| cp source destination                    | Copy file source to destination                                            |
| cp -p source destination                 | Copy file and preserve the mode, ownership and timestamp                   |
| cp -r source destination                 | Copy directory source to destination recursively                           |
| mv source destination                    | Move/rename file or directory source to destination                        |
| touch file                               | Create or update file                                                      |
| cat file                                 | Output the contents of file                                                |
| tac file                                 | Output the contents of file, in reverse order, beginning at the end        |
| head file                                | Output the first 10 lines of file                                          |
| tail file                                | Output the last 10 lines of file                                           |
| tail -f file                             | Output the contents of file as it grows, starting with the last 10 lines   |
| vim file                                 | Edit file with the Vim editor                                              |
| *                                        |                                                                            |
| ?                                        |                                                                            |
| [a-z]                                    |                                                                            |
| [0-9]                                    |                                                                            |
| convert                                  | converts the output of a command in picture, automatically                 |
| du -hsx * &#124; sort -rh &#124; head -6 | top 6 files that eat up your space                                         |
| du -h --max-depth=1                      |                                                                            |
| file                                     | Filetype                                                                   |
| find -size +100M                         |                                                                            |


Searching
---------

| Command                              | Description                                                                        |
| :----------------------------------- | :--------------------------------------------------------------------------------- |
| grep pattern files                   | Search for pattern in files                                                        |
| grep -r pattern dir                  | Search recursively for pattern in dir                                              |
| grep -rn pattern dir                 | Search recursively for pattern in dir and show the line number found               |
| grep -r pattern dir --include='*.ext | Search recursively for pattern in dir and only search in files with .ext extension |
| command &#124; grep pattern          | Search for pattern in the output of command                                        |
| find file                            | Find all instances of file in real system                                          |
| updatedb && locate file              | Find all instances of file using indexed database built from the updatedb command  |


Networking
----------

| Command                           | Description                                                                           |
| :----------------------------     | :------------------------------------------------------------------------------------ |
| wget file                         | Download a file                                                                       |
| curl file                         | Download a file                                                                       |
| scp user@host:file dir            | Secure copy a file from remote server to the dir directory on your machine            |
| scp file user@host:dir            | Secure copy a file from your machine to the dir directory on a remote server          |
| scp -r user@host:dir dir          | Secure copy the directory dir from remote server to the directory dir on your machine |
| ssh user@host                     | Connect to host as user                                                               |
| ssh -p port user@host             | Connect to host on port as user                                                       |
| ssh-copy-id user@host             | Add your key to host for user to enable a keyed or passwordless login                 |
| ping -c 5 host                    | Ping host and output limited to 5 results                                             |
| whois domain                      | Get information for domain                                                            |
| dig domain                        | Get DNS information for domain                                                        |
| dig -x host                       | Reverse lookup host                                                                   |
| netstat -tulpn &#124; grep LISTEN | List all open ports                                                                   |
| lsof -i tcp:80                    | List all processes running on port 80                                                 |
| curl ifconfig.me                  | External IP                                                                           |
| curl ipinfo.io                    |                                                                                       |


Permissions
-----------

| Command                                              | Description                                                 |
| :--------------------------------------------------- | :---------------------------------------------------------- |
| ls -l                                                | List items in current directory and show permissions        |
| stat file                                            | Shows the status information of a file                      |
| getfacl file                                         |                                                             |
| chmod ugo file                                       | Change permissions of file (u = user, g = group, o = other) |
| 0 or -                                               | No permissions                                              |
| 1 or x                                               | Execute                                                     |
| 2 or w                                               | Write                                                       |
| 4 or r                                               | Read                                                        |
| 3 or wx                                              | (1 + 2) Write and execute                                   |
| 5 or rx                                              | (1 + 4) Read and execute                                    |
| 6 or rw                                              | (2 + 4) Read and write                                      |
| 7 or rwx                                             | (1 + 2 + 4) Full permissions                                |
| find /dir/ -type d -exec chmod 755 {} +              |                                                             |
| find /dir/ -type f -exec chmod 644 {} +              |                                                             |
| find /dir/ -type d -name "dir" -exec chmod 755 {} +  |                                                             |
| find /dir/ -type f -name "file" -exec chmod 644 {} + |                                                             |
| chown -R root:www-data /dir/                         |                                                             |
| usermod -aG sudo else                                | User else in gruppe sudo aufnehmen                          |


Compression
-----------

| Command                   | Description                                  |
| :------------------------ | :------------------------------------------- |
| zip file                  | Compresses file and renames it to file.zip   |
| unzip file.zip            | Decompresses file.zip back to file           |
| gzip file                 | Compresses file and renames it to file.gz    |
| gzip -d file.gz           | Decompresses file.gz back to file            |
| bzip2 file                | Compresses file and renames it to file.bz2   |
| bzip2 -d file.bz2         | Decompresses file.bz2 back to file           |
| tar cf file.tar files     | Create a tar named file.tar containing files |
| tar xf file.tar           | Extract the files from file.tar              |
| tar czf file.tar.gz files | Create a tar with Gzip compression           |
| tar xzf file.tar.gz       | Extract a tar using Gzip                     |


Services
--------

| Command              | Description                      |
| :------------------- | :------------------------------- |
| service ssh status   | Check the status of a service    |
| service --status-all | Check the status of all services |
| service ssh start    | Start a service                  |
| service ssh restart  | Restart a service                |
| service ssh stop     | Stop a service                   |
| journalctl -xe       |                                  |


Shortcuts
---------

| Command       | Description                                      |
| :------------ | :----------------------------------------------- |
| Tab+Tab       |                                                  |
| Alt+Backspace | Deletes the previous word                        |
| Alt+F         | Skips ahead to the next space                    |
| Alt+B         | Skips back to the previous space                 |
| Ctrl+U        | Cuts all text up to the cursor                   |
| Ctrl+K        | Cuts all text after the cursor until end of line |
| Ctrl+A        | Moves the cursor to the start of line            |
| Ctrl+E        | Moves the cursor to the end of line              |



Fun
---

| Command                                  | Description                  |
| :-----------------------------------     | :--------------------------- |
| cmatrix                                  |                              |
| echo "long source code" &#124; pv -qL 20 |                              |