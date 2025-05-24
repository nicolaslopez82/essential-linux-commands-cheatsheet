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
