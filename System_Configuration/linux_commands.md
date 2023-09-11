# Linux Commands

## System Admin & Basics

`xdg-open /` Open GUI to root/top-level directory | `open [file-name]`

`sudo apt update` Update System

`sudo apt upgrade` Upgrade System

`sudo apt full-upgrade` Update All Programs

`sudo su` Become Root User

`id` Display Root User

`exit` or `Ctrl + d` Exit Root User

`sudo passwd [root]` Change Password for Root

`Control + Alt + l` Clears the Screen

`Control + d` Closes the Shell

`bindkey -L` Display all listed key binds

`Alt + Space` Fuzzy Finder

`cron` Commands

`-l` Displays all `cron` jobs

`-e` Edits `crontab` file

`mount` Command

`-o rwe` Assign Read/Write/Execute Permissions

`sudo mount [device-name] [directory-name]` Mount device to desired directory

`sudo unmount [directory-name]` `Unmount` Directory

`dd` Command

`sudo dd if=[directory-name] [status=progress]` Clone/Copy data

`lscpu -json | less` Displays hardware information

`inxi -Fx` Displays hardware information

`lscpu` CPU information

`dmidecode` Amount of memory free

`lsusb` Information on USB/devices

`dparm` Details on Hard disk drives/ benchmark hard disks

`systemd` Service manager

`systemctrl` Manage Services

## User Account Management

`sudo useradd [user-name]` Create new user

`sudo passwd [user-name]` Set new password for user

`su [user-name]` Change to user

## **Navigation Basics**

`Control + p` Previous Command

`Control + n` Next Command

`Control + f` Move one character at a time

`Control + b` Move one character at a time

`Alt + f` Move one word at a time

`Alt + b` Move one word at a time

`Control + a` Takes you to the beginning of the line

`Control + e` Takes you to the end of the line

## E**dit Basics**

`Control + m` Enter

`Control + i` Tab

`Control + z` Undo

`Control + Shift + u` Emoji Selection

`Control + d` Delete character right of cursor

`Alt + d` Delete the word right of cursor

`Control + w` Delete character left of cursor

`Alt + w` Delete word left of cursor

`Control + k` yank pop

`Control + y` Yank right of cursor to clipboard

`Alt + y` Yank left of cursor to clipboard

`Alt + v` Paste last yank

`Control + x + Control + x` Highlight

`Control + t` Swap characters

`Alt + t` Swap words

`Alt + c` Upper case letter

`Control + u` Lower case all letters to end of word

`Alt + u` Upper case all letters to end of word

## **History Basics**

`history`

`!{number}` Use command from history

`Control + r` Search through history

`history Command:p` Print the command

`history -c` clear History

`[space] [command]` Leave space to not have command show in history

## **Manual Basics**

`man` Manual Command

`spacebar` Move `1` page at a time

`b` Move `1` page back at a time

`g` Move to start if Man page

`man` pages use `h` Help Commands

`man` pages use `/[search-term]` Search Function

`man -k echo` Displays all pages that contains keyword **echo**

`type [command]`  Where or how a command is defined

`which` Where a command is located

`help` Commands not within Manual

`file` Command that prints file format/extension

## File System

`/` Root Directory

`~` or `home` Home Directory

`/home/nathan/Dev/Projects` Absolute Path

`cd ../Projects` Relative Path

`df` Display Disk Space

`df -h`

`cd` Change Directory

`pwd` Print Working Directory

`du` Disk Usage

`ls` Lists All Directories

`ls /` Lists all folders

`\ls` Removes colours

`ls [directory]` Lists All Directories In Selected Directory

`ls -l` Long List

`ls -a` All

`ls -h` Human Format

`ls -lS` Files Sorted By Size

`ls -lR` Runs Recursively

`ls -li` index node `inode` data structure of each file

`ls -F` Sort By Modification Time

`ls -lu` Last Time The File Was Read

`ls -lt` Last Time The Contents of The File Was Modified

`ls -lc` Last Time When Some Metadata Related to The File Was Changed

`ls -l --full-time` Shows Full Time

`stat [directory]` Detailed Info On Directory or File

`cat [file-name]` Displays Content of File

`cat [file-name-1] [filename-name-1]` Concatenate files

`less [file]`

`watch l` Runs `ls` command every 2 seconds

`head` | `head -n 2` Prints first 2 lines from file.

`tail` | `head -n 2` Prints last 2 lines from file.

`mkdir [directory-name]` Create Directory

`-v` Verbose Option

`-p` Parent Option — `mkdir dir1/dir2/dir3 -p`

`touch [file-name]` Create File

If exists `touch` will update timestamps to current time

`-r` Recursive Option

`cp [source] [destination]` Copy File or Folder

`-v` Verbose Option

`-p` Preserve Option

`-i` Interactive Option

`mv [source] [destination]` Move / Renames Files or Folders

`mv *.txt` Moves all files with `.txt` file extension

`rm` Remove Files

`-i` Interactive Option

`-v` Verbose Option

`rm -d` or `rmdir` Removes Empty Directories

`rm -f` Force Remove

`rm -r` or `rm -R` `rm --recursive` Remove Directories or Files

`shred` Overwrite Content of Files Before Removing It

`|` Chain Multiple Commands Together

`STDIN (0)` Standard Input

`cat [Directory name] | grep -a "phrase"` Prints all lines with “phrase”

`STDOUT (1)` Standard Output

`>` Output Redirection Operator

`>>` Append operator

`[number]>` Redirects Number Stream

`STDERR (2)` Standard Error

`2>` or `2>>` Redirect Standard Error

`2>&1` Redirect Standard Error Into Output

`cat error.txt | grep ls | tee work.txt` `tee` Command allows to print and save

## Compare Files

`cmp [file-name-a] [file-name-b`] Compares Both Files

`diff [file-name-a] [file-name-b`] Displays Differences Between Both Files

`sha256sum [file-name-a] [file-name-b`] Displays `sha256` of Both Files

## Search

`find` Command

`find . -name [file-name]` Find in Current Directory & Sub Directories

`..` Parent Directories

`find . -iname` Ignore Case

`find . -name [file-name] -delete` Deletes file once found

`find . -type [type]` `d`Directories `f` Files

`find .-maxdepth [number]` Finds n levels down

`find . -size [number k]` Find files with a size of n

`find . -type f -exec cat{} \;` Execute `cat` on all files found

`grep` Command

`grep [pattern] [file-name]`

`-i` Ignore case

`-n` Print line number

`-w` Search pattern

`-v` Inverts Search

`-a` Search in Binary file

`-R` Search string within Directories

`-s` Suppress errors

`-c` Outputs number of matches | or can pipe with `wc` Command

## Compressing and Archiving Files and Directories

`tar` Command

`tar -chzvf [specified-name.tar.gz] [selected dir/file-name]`

`-c` Create a Archive

`-z` Filter the archive through `gzip`

`-j` Filter the archive through `bzip2`

`-v` Verbose Option

`-f file.tar.gz` Use archive file

`tar -xzvf [Archived File]` Unzip Archived File

`-j` Filter The Archive through `bzip2` (Replace `z` flag with `j` flag)

`-C [specified-name.tar.gz]` Extract Archived File Within Specified Directory

`tar -xzvf [specified-name.tar.gz] -exclude='specified' [selected dir/file-name]` Excludes Folders/Files

`tar -xzvf [archived-file.tar.gz] -C [selected dir]`

`-x` Extract files from an archive

`-t` List the contents of an archive

`-v`Verbose output

`-f file.tar.gz` Use archive file

`C DIR` Change to DIR before performing any operations

`-exclude` Exclude files matching PATTERN/DIR/FILENAME

## File **Permissions**

`drwxrwxr-x`

First Character:

`x` File type

`l` Links (shortcut)

`d` Directory

`b` Block device

`c` Char devices — logical

`s` Socket

`p` Named pipe

`drw-rw-r--x`

First 3 letters `rw-` File Owner Permission

Second 3 letters `rw-` Group Owner Permission

Last 3 letters `r--` World Permission

`drwxrwxr-x`

`r` Read permission

`w` Write permission

`x`  Execute permission

`Octal/Numeric Notation`

`r is 4`

`w is 2`

`x is 1`

`- is 0`

`rwxr---wx is 743`

`chmod [WHO] [OPERATIONS] [PERMISSIONS] filename` Change modes

`WHO`

`u` User

`g` Group

`o` Others

`a` All

`OPERATIONS`

`-` Remove

`+` Grants

`=` set a permission and removes others

`PERMISSIONS`

`r` Read

`w` Write

`x` Execute

`chown` Change Owner

`chown [specified-new-user] [file-name]`

`chgrp` Change Group

`chgrp [specified-new-group] [file-name]`

`SUID` Permissions of Owner

Absolute Mode: `chmod 4XXXX file`

Relative Mode: `chmod u+s file`

`SGID` File/Directory owned by group owner of the directory where `SGID` was configured.

Absolute Mode: `chmod 2XXXX directory`

Relative Mode: `chmod g+s directory`

`Sticky Bit` Only delete files that you own for which you have explicit write permission.

Absolute Mode: `chmod 1XXXX directory`

Relative Mode: `chmod o+t directory\`

`umask` Command

Default Permissions: `0666` Files | `0777` Directory

## Linux Process Management

`type [linux-command]` Command

`Shell builtin`

`Exac File`

`top` Dynamic real-time view of a running system | `htop`

`1` Show CPU(s)

`t` Change Graphs

`m` Display Memory

`b` Highlight

`<` or `>` to navigate through options

`ps` Process Status

`-e` Display all processes

`-f` Detailed information

`pgrep -l [process-name]` Searches for processes

`pstree` Displays process tree

`Control + c` Kill Command

`kill -l` Lists `kill` commands

`kill -[kill number] [process IDs]` Kills program based on process IDs

`killall -[kill number] [process name]` Kill all processes

`pkill -[kill number] [process phase]` Kills process on partial name

## Networking

`ip` Command

`ip a show` or `ip a` Display Network Information

`ifconfig` Display Network Information

`sudo ip link set [interface-name] [disable/enable]`Enable/disable Interface

`route` or `route -n` Display `Gateways`

`resolvectl status` Display `DNS`

`ping` Command — Troubleshooting Network

`-i [0.4]` Sets time interval of packets sent

`-c [5]` Number of packets transmitted

`SSH (Secure Shell)`

`systemctl status ssh` Validate SSH running
