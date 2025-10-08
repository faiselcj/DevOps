Linux commands



APT

. apt install sudo - to install (lib,package)

. sudo apt update - to update (up to date)

. sudo apt upgrade -y (latest version)



&nbsp; list - list packages based on package names

&nbsp; search - search in package descriptions

&nbsp; show - show package details

&nbsp; install - install packages

&nbsp; reinstall - reinstall packages

&nbsp; remove - remove packages

&nbsp; autoremove - automatically remove all unused packages

&nbsp; update - update list of available packages

&nbsp; upgrade - upgrade the system by installing/upgrading packages

&nbsp; full-upgrade - upgrade the system by removing/installing/upgrading packages

&nbsp; edit-sources - edit the source information file

&nbsp; satisfy - satisfy dependency strings



USER MANAGEMENT

1.useradd demo -- creating user without home DIR

2.useradd -m demo -- creating user with home DIR

3.passwd demo -- to create password for user without DIR

4.cat etc/passwd -- to check user is created

5.adduser demo-- creating user with home DIR

6\. useradd -s /bin/bash <name> -To specify a shell

7.cat etc/shadow



password policy



8.chage -M 90 <user> - to make user change password every 90 days

9.passwd -i <user> -- lock a user

10.passwd -u <user> -- unlock a user


modify user

11.usermod -l <new\_username> <old\_username> -- rename user name

12.usermod -d /new\_dir -m <username> -- change user from one to another dir


DELETE User

13.userdel -r <username> -- delete user with dir

14.userdel <username> -- delete user



Group creation



15.groupadd <name>

16.usermod -aG <groupname> <username>

17.groups <username> - to check members in groups

18.cat etc/groups

###### 

###### Add  sudo Access and Privilege Escalation



19.usermod -aG sudo <username>



###### File management in Linux

###### File and Directory Management

1. 1 . ls – Lists files and directories in the current location.
2. cd /path/to/directory – Changes the working directory.
3. pwd – Prints the current working directory.
4. mkdir new\_folder – Creates a new directory.
5. mkdir -m=rwx <dir\_name> - create new dir with permission
6. mkdir -p parent/child/subchild -- create parent child dir
7. rmdir empty\_folder – Removes an empty directory.
8. rm file.txt – Deletes a file.
9. rm -r folder – Deletes a folder and its contents.
10. cp file1.txt file2.txt – to create a Copies of a file.
11. cp -r dir1 dir2 – Copies a directory recursively.
12. mv old\_name new\_name – Moves or renames a file or directory.
13. mv demo.md /tmp/ -- move file and folder
14. mv file1.txt file2.txt /home/faisel/docs/





###### 

###### File Viewing and Editing

1. cat file.txt – Displays file content.
2. tac file.txt – Displays file content in reverse order.
3. less file.txt – Opens a file for viewing with scrolling support.
4. more file.txt – Similar to less, but only moves forward.
5. head -n 10 file.txt – Displays the first 10 lines of a file.
6. tail -n 10 file.txt – Displays the last 10 lines of a file.
7. nano file.txt – Opens a simple text editor.
8. vi file.txt – Opens a powerful text editor.
9. echo 'Hello' > file.txt – Writes text to a file, overwriting existing content.
10. echo 'Hello' >> file.txt – Appends text to a file without overwriting.

    File Permissions Management in Linux

    chmod u+x filename  # Add execute for user
    ---
12. ###### chmod g-w filename  # Remove write for group
13. ###### chmod o=r filename  # Set read-only for others
14. ###### chmod u=rwx,g=rx,o= filename  # Set full access for user, read/execute for group, and no access for others
15. ###### chmod 755 filename  # User (rwx), Group (r-x), Others (r-x)
16. ###### chmod 644 filename  # User (rw-), Group (r--), Others (r--)
17. ###### chmod 700 filename  # User (rwx), No access for others


Modify file owner and group:
---

###### 

1. ###### chown newuser filename  # Change owner
2. ###### chown newuser:newgroup filename  # Change owner and group
3. ###### chown :newgroup filename  # Change only group
