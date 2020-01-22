# Command Line Cheat Sheet

## Help

`man <command>`
- display the 'manual page' for a command

`<command> --help`
- display a command's help screen


## Directories

`pwd`
- Display the present working directory

`cd <directory>`
- Change to specified directory

`cd ..`
- Change to parent directory

`cd` or `cd ~`
- Return to home folder

`ls`
- List files in present working directory

`ls <directory>`
- List files in specified directory

`ls -la`
- List files in a detailed format, including hidden files

`mkdir <directory>`
- Create a new directory


## Directory Paths

`.`
- Current directory

`..`
- Parent directory

`~`
- Home directory

`/path/to/files/`
- Absolute path
- Always begins at root (`/`)

`path/to/directory`
- Relative path
- Always begins at present working directory


## Files

`touch <file>`
- Create a file if it does not exist
- Update file modification time

*Note:* The following commands may be destructive, overwriting existing files! Use with caution!

`mv <file-old> <file-new>`
- Rename filename (old) to filename (new)

`mv <file> <directory>`
- Move specified file into specified directory

`cp <file> <directory>`
- Copy specified file into specified directory

`cp -r <directory-1> <directory-2>`
- Copy directory-1 into directory-2


## Deleting

**WARNING!** Deleting a file or directory using any of the following commands is *PERMANENT*. There is no way to recover deleted files!

`rm <file>`
- Delete specified file

`rm -r <directory>`
- Delete specified directory

`rm -f <file>`
- Force delete the specified file

`rm -rf <directory>`
- Force delete the specified directory

`rm -rf *`
- NEVER TYPE THIS COMMAND. It will delete EVERYTHING!


## Output

`echo <string>`
- Show contents of the string on the screen (a.k.a "standard output")

`cat <file>`
- Show the contents of the specified file

`less <file>`
- Show the contents of the specified file, paginated
- `space` to scroll forward one page
- `b` to scroll backward one page
- `q` to quit

`head <file>`
- Display the first 10 lines of the specified file

`<command> > <file>`
- Direct output from the command to the file
- Note: May overwrite the content of an existing file!

`<command> >> <file>`
- Append output from the command to the specified file

`<command-1> | <command-2>`
- Direct the output from command-1 to command-2


## Search

*See also: Wildcards*

`find <directory> -name "<file>"`
- Find files with the given name inside the specified directory

`grep "<text>" <file>`
- Search for text provided in specified file

`grep -rl "<text>" <directory>`
- Search for text provided in all files within the specified directory


## Editors

`nano` or `nano <file>`
- simple
- To quit: `ctrl-x` (`^x`)

`emacs` or `emacs <file>`
- complex
- To quit: `ctrl-x` then `ctrl-c` (`^x ^c`)

`vi` or `vi <file>`
- complex
- To quit: type `:`, then `q!`


## Wildcards

`*`
- match any (zero or more characters)
- `*all` would match "all", "ball", "call", "small", etc.

`?`
- match a single character
- `?all` would match "ball", "call" but not "all", "small"


## Network Utilities

`ping <host>`
- Ping host, display stats
- `^c` to exit

`whois <domain>`
- Display domain name data

`curl -0 <url/to/file>`
- Download file via http(s) or ftp

`ssh <username>@<host>`
- Connect via secure shell to host; log in using username
- May require a 'public key'

`scp <path/to/file> <user>@>host:/remote/path>`
- (Secure) Copy file to remote <host>


## Utilities

`whoami`
- In case you forgot :)

`clear`
- Clears the screen

- `wc`
- Word count; displays lines, words, characters

`uniq`
- List unique output

`sort`
- Sort output alphabetically

`sort -n`
- Sort output numerically


## Permissions

Because users share a system, files and directory have metadata as to who can read (`r`), write to (`w`) or execute (`x`) a file. Unix/Linux systems classify those who can access files as the user (you) (`u`), a group (`g`) or other/everyone (`o`).

### Commands

`chmod <permission> <file/directory>`
- Change the permission of a file/directory

`chmod -R <permission> <directory>`
- Change the permission (and files within)

`chown <user> <file/directory>`
- Change the ownership of a file/directory
- Include `-R` to include contents within a directory

### Symbolic Method

`<who><+/-><permission>`

`u+rw`
- Give the user read and write access (no execute)

`o+rx`
- Give all read, execute access (no write)

`o-rw`
- Revoke read, write access for all

### Octal Method

We can also indicate permissions for each group by adding numbers. Read, write and execute are represented by numbers:

`4`: read<br/>
`2`: write<br/>
`1`: execute

The permission is three digits (`xxx`) with the hundreds column representing the user, tens representing groups and the ones representing all.

`755`
- User has all access. group and others can read and execute.

`600`
- User has read, write access; group and others have no access.

`644`
- User has read, write access; group and others can only read.


## Quick Tips

- Use the `TAB` key to autocomplete paths.

- Use `↑` (arrow up) and `↓` (arrow down) to cycle through the commands recently used.

- `ctrl-a` (`^a`) will move your cursor to the start of the line.

- `ctrl-e` (`^e`) will move your cursor to the end of the line.

- `ctrl-k` (`^k`) deletes all text ahead of the cursor.

- `ctrl-l` (`^l`) clears the screen

- `ctrl-c` (`^c`) aborts a command


## What do I use to...?

- create a file
`touch` or `nano` (or your editor of choice)

- view contents of a file?
`cat` or `less`

- view contents of a directory?
`ls`

- navigate to...?
`cd`

- move a file or directory?
`mv`

- copy a file?
`cp`

- copy a directory?
`cp -r`

- delete a file?
`rm`

- delete a directory?
`rmdir`
