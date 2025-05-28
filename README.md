# Essential Linux Commands Cheatsheet 

## Navigation & File Management 

`pwd` - Print working directory.

`ls` - List files and directories.

`ls -l` - Long format.

`ls -a` - Show hidden files.

`ls -h` - Human-readable sizes.

------------

## File Operations 

`cat [filename]` - Display file contents.

`less [filename]` - View with pagination.

`head [filename]` - Show first 10 lines.

`tail [filename]` - Show last 10 lines.

`tail -f` - Follow file updates in real-time.

`grep [pattern] [file]` - Search for pattern.

`grep -i` - Case sensitive.

`grep -r` - Recursive search.


`diff [file1] [file2]` - Compare files.

`wc [file]` - Count lines, words, bytes.

`wc -l` - Prints the number of lines in file.

`wc -w` - Prints the number of words in file.

`wc -m` - Prints the count of characters.

------------
## Find Operations 

`find` - Search files with various options.

Commons options: `type`, `name`, `size`

#### Example:

`find . -name "*.log"` - Starting from the current directory, search through all subdirectories and find any files that have a name ending with '.log' 

------------
## File Permissions

Format: `rwx rwx rwx` (owner group others)
- `r` (4): Read permission.
- `w` (2): Write permission.
- `x` (1): Execute permission.

Common examples:
- `chmod 755` - Owner full access, others read/execute.
- `chmod 644` - Owner read/write, others read only.
- `chmod 700` - Owner full access, others none.

------------
## Vim Text Editor

#### Normal Mode (default):

`h, j, k, l` - Move cursor.

`dd` - Delete Lines

`yy` - Copy line.

`p` - Paste.


#### Insert Mode (press `i`):

Type to insert text
`Esc` - Return to Normal mode.


#### Command Mode (press `:`):

`:w` - Save.

`:q` - Quit.

`:wq` - Save and Quit.

## Piping & Redirection

`|` - Pipe output to next command.

`> [file]` - Redirect output (overwrite).

`>> [file]` - Append output.

`2> [file]` - Redirect errors.

### Examples:

`ls -l | grep "\.txt"` - Shows detailed listing of only .txt files.


`command > out.txt 2> errors.txt` - Saves normal output to one file and error messages to another file.

## System & Process

`ps` - Show process.

`ps -ef` - All processes in full format.

`ps aux` - Detailed process list.


`top` - Real-time process monitor.

`kill pid` - Terminate process.

`df -h` - Show disk space.

`free -h` - Show memory usage.


## SSH & Remote Access

`ssh user@hostname` - Connect to server.

`ssh-keygen` - Generate SSH key pair.

`ssh-copy-id user@host` - Copy SSH key.

`scp file user@host:path` - Copy file.

## Command History

`history` - Show history.

`!!` - Execute last command.

`Crtl + R` - Search history.

## Package Management
`apt update` - Update package list.

`apt install pkg` - Install package.

`apt remove pkg` - Remove package.

`apt upgrade` - Upgrade packages.

## Root Access

`sudo command` - Run as root.

`sudo su` - Become root.

`passwd` - Change password.

## Network Commands

`ping` - Test connectivity.

### Example:

`ping -c 4 google.com` - Tests the connectivity between your computer and Google's servers. `-c 4` limits the test to 4 packets.

`curl` - Transfer data from/to server.

### Example:

`curl -I https://example.com` - Checks if a website is up without downloading the entire page content. `-I` tells curl to send a HEAD request instead of the default GET request.

`netstat` - Display network statistics.

## Example:

`netstat -tuln`

`-t` Shows TCP connections.

`-u` Shows UDP connections.

`-l` Display only listening sockets (servers).

`-n` Shows numerical addresses instead of resolving hostnames and port numbers.

## System Information

`uname` - Show system information.

`who` - Show who is logged in.

`hostname` - Show or set hostname.

`free` - Display memory usage.
