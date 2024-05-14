### File System Hierarchy in Linux

#### Root Directory
- `/root`: Home directory for the root user.
- `/home/username`: Home directories for non-root users.

#### Executable Directories
- `/bin`, `/usr/bin`, `/usr/local/bin`: Directories for user-executable files.
- `/sbin`, `/usr/sbin`, `/usr/local/sbin`: Directories for system-executable files, accessible only by the root user.

#### Mount Points
- `/media`, `/mnt`: Directories for mount points.

#### Configuration
- `/etc`: Directory for configuration files.

#### Temporary Files
- `/tmp`: Directory for temporary files.

#### Boot Files
- `/boot`: Directory for kernels and bootloaders.

#### Server Data
- `/var`, `/srv`: Directories for server data, such as website files and sometimes SQL databases.

#### System Information
- `/proc`, `/sys`: Directories for system information.

#### Shared Libraries
- `/lib`, `/usr/lib`, `/usr/local/lib`: Directories for shared libraries.

### Types of files in Linux
- **Regular Files**: Contain data, text, or program instructions.

- **Directories**: Contain other files and directories.

- **Symbolic Links**: Point to other files or directories.

- **Device Files**: Represent hardware devices.

- **Named Pipes**: Allow inter-process communication.

- **Sockets**: Allow communication between processes.

- **Special Files**: Represent system resources.

### Steps to make links in Linux
- **Hard Links**: Point directly to the file's inode, and changes to the original file are reflected in the hard link.


### grep command
- `grep` is a command-line utility for searching plain-text data sets for lines that match a regular expression.
- `grep [options] pattern [files]`
- `grep -i`: Ignore case.
- `grep -R`: Search recursively.
- `grep -iR "pattern" /path/to/dir/`

- `grep -v`: Invert match.
- `grep -v "pattern" file.txt`


### less command
- `less` is a command-line utility for viewing text files.

### more command
- `more` is a command-line utility for viewing text files.

## head command
- `head` is a command-line utility for displaying the first few lines of a file.
- `head -n 5 file.txt`: Display the first 5 lines of a file.

## tail command
- `tail` is a command-line utility for displaying the last few lines of a file.
- `tail -n 5 file.txt`: Display the last 5 lines of a file.
- `tail -f file.txt`: Display the last 10 lines of a file and update the display as the file changes. `Useful for monitoring log files.`
- `tail -F file.txt`: Same as `-f`, but will continue to track the file even if it's renamed or rotated.

### awk command
- `awk` is a command-line utility for processing text files.
- `awk '{print $1}' file.txt`: Print the first column of a file.

### sed command
- `sed` is a command-line utility for processing text files.
- `sed 's/old/new/g' *`: Replace all occurrences of `old` with `new` in all files.

### /dev/null
- `/dev/null` is a special file that discards all data written to it.
- `cat /dev/null > file.txt`: Clear the contents of a file.

### 2>>, 1>> and &>>
- `2>>`: Append standard error to a file.
- `1>>`: Append standard output to a file.
- `&>>`: Append both standard output and standard error to a file.

### pipe (|)
- The pipe (`|`) operator is used to combine two or more commands.
- `command1 | command2`: Pass the output of `command1` as input to `command2`.  
- `ls -l | grep "file"`: List files and filter the output to show only lines containing "file".

### visudo
- `visudo` is a command-line utility for editing the sudoers file.
- `visudo -f /etc/sudoers.d/myfile`: Edit a specific sudoers file.