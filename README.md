# Day 1 to 3-Linux
I’m practicing daily to strengthen my foundational skills in Linux, Bash scripting, and DevOps tools.
| Day | Topic | Key Learnings |
|-----|-------|----------------|
| 01  | Basics | mkdir, ls , pwd, touch, clear, rm, rm dir, echo, cat, zcat |
| 02  | Permissions |chmod, chown,chgrp|
| 03  | File Mgmt | zip, unzip, gunzip, tar |


**DAY -01**

1. `pwd` – Print Working Directory
   -> Shows the **current directory** you're in.
    ```bash
    pwd
    O/P: /home/ubuntu/projects
2. ls – List Directory Contents
   ls           # basic listing
   ls -l        # detailed list (permissions, size, owner, date)
   ls -a        # shows hidden files too
   ```bash
   ls -la

3. cd – Change Directory
   cd folder_name        # move into folder
   cd ..                 # move one level up
   cd /path/to/folder    # move using absolute path
   cd ~                  # move to home directory

   ```bash
   cd /etc/nginx

4. mkdir – Make Directory->Creates a new folder (directory).
   mkdir myfolder
   mkdir -p a/b/c    # creates nested folders

   ```bash
   mkdir devops-notes

5. touch – Create New File-> Creates a new empty file.

   ```bash
   touch filename.txt

6. rm – Remove File or Directory-> rm – Remove File or Directory
   rm file.txt             # remove a file
   rm -r folder/           # remove a folder recursively
   rm -rf folder/          # force delete folder and contents

   ```bash
   rm -rf testfolder

7. echo-> Print Text or Variables-> Displays a line of text or the value of a variable.
  ```bash
   echo "Hello, World!"
   echo $HOME                     # shows current home directory
   echo "Welcome to DevOps" > msg.txt   # writes to a file
   echo "Another line" >> msg.txt       # appends to a file#
```
8. cat – Concatenate and Display File Contents
 ```bash
   cat filename
   cat file1.txt                    # shows contents
   cat file1.txt file2.txt          # shows both files
   cat > newfile.txt                # create new file (Ctrl+D to save)
   cat >> existingfile.txt          # append to a file #
````

9. zcat – View Contents of Compressed (.gz) Files

   ```bash
   zcat file.gz
   zcat logs.tar.gz                 # view compressed log
   ```

**DAY-02**

1. Check File Permissions – ls -l

   ls -l filename
   ex-> -rw-r--r-- 1 user group 1024 Aug  7 12:34 file.txt
   - = file (d for directory)

   rw- = owner (read/write)

   r-- = group (read-only)

   r-- = others (read-only)

2. Change Permissions – chmod

   chmod u+x script.sh   # Add execute to user
   chmod g-w file.txt    # Remove write from group
   chmod o=r file.txt    # Set read-only for others

3. Change Ownership – chown

   chown newuser file.txt         # Change owner
   chown newuser:newgroup file.txt # Change owner & group

 4. Change Group – chgrp

    chgrp devs file.txt
    

**DAY-03**

1. zip – Compress Files into a .zip Archive

   zip archive.zip file1.txt file2.txt
   zip -r folder.zip myfolder/

2. unzip – Extract Files from a .zip Archive
   unzip archive.zip

3. gzip – Compress a File Using .gz Format

   gzip filename.txt          # Creates filename.txt.gz and deletes original
   gzip -k filename.txt       # Keeps original file

4. unzip – Decompress .gz Files
   gunzip filename.txt.gz

5. tar – Archive and Compress Multiple Files

   tar -cvf archive.tar file1 file2         # Create archive
   tar -xvf archive.tar                     # Extract archive
   tar -czvf archive.tar.gz folder/        # Create compressed tarball
   tar -xzvf archive.tar.gz                # Extract compressed tarball

Networking :

1. ping – Test Network Connectivity

   ping google.com
   ping -c 4 google.com

2. ifconfig / ip addr – Show IP Information
   ifconfig
   ip addr
   
3. netstat – Show Network Connections (use ss instead in modern systems)
   netstat -tuln
   ss -tuln

4. curl – Make HTTP Requests
   curl https://example.com
   curl -I https://example.com

5. wget – Download Files
   wget https://example.com/file.zip

6. traceroute – Trace Route to Host
   traceroute google.com

7. nslookup / dig – DNS Lookups
   nslookup google.com
   dig google.com

















