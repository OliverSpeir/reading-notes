# Command Line Tutorials
- [Bash Command Line Turotials by ryanstutorials.net](https://ryanstutorials.net/linuxtutorial/)

## The Command Line
- This section focuses on the basics of how to open the terminal on different operating systems
- This section also defines what a shell is, and explains that bash stands for Bourne Again Shell 
- I am using Z shell
- <img src="https://i.imgur.com/iR9rkga.png" />

## Basic Navigation
- `pwd` tells you what directory you are in and the path to that directory
- `ls` lists everything that is in the directory you are in
-  `ls [options] [location]` 
- Absolute vs Relative Paths 
- `/` is root directory
- Absolute path has `/` 
- Relative path does not need to start with `/`
- `~` is a shortcut for home directory
- `.` is a reference  to your current directory
- `..` is a reference to the parent directory of your current directory
- My username is "a1" for reference 
- `cd` stands for change directory
- `cd [location]`
- Activity: get to home directory using 4 different methods
- <img src ="https://i.imgur.com/zp4fPu7.png"/>

## More About Files
- Everything is a file
- linux does not use file extensions 
- if file extensions are seen in linux they are for the user only
- a picture will open in linux with .png or .txt extension
- `file [path]` is a command that will tell the user what type of file it is
- linux is case sensitive
- spaces in names are tricky as space denotes the end of a command
- can use escape character or single quotes 
- `cd 'Holiday Photos'`
- `cd Holiday\ Photos`
- hidden files are denoted by . before the file
- `.zshrc` is an example of a hidden file
- `ls -a` shows hidden files
- Activity: run file command and ls -a
- <img src ="https://i.imgur.com/MMG4nsz.png"/>

## Manual Pages
- every command has a manual page 
- `man [command]`
- `man ls` for example
- `man -k [term]`   searchs all man pages
- `/[term]` while viewing man page searches and pressing `n` cycles through the results
- `--` is long hand for command options
- when shorthand is used for options can chain them all together
- `ls --all` or `ls -a`
- `ls -alh` is all three options -a -l -h
- activity: use ls with aboslute path and search a man page
- <img src ="https://i.imgur.com/t9aOdz4.png"/>
- <img src ="https://i.imgur.com/9t9I4ws.png"/>
- <img src ="https://i.imgur.com/RqFaYOm.png"/>

## File Manipulation
- Make directories so that you can find your files easily
- `mkdir [options] <directory name or path if using -p option>`
- -p option to mkdir creates parent directories necessary to make the path we give it accurate 
- -v option has the command return what it has done such as parent directories made if -p is used
- `rmdir [options] <directory name or path>`
-  `touch [options] <file name>` creates a blank file
- `cp [options]<source path><destination path>` copies a file or directory
- `mv [options]<source path><destination path>` moves a file or directory
-mv can be used to rename a file 
-`mv foo foo2`  renames foo to foo2
- `rm [options] <file or path>`
- `rm -r` is necessary for directories 
- `rm -rf` to avoid having to accept every file 
- Activity: 
- <img src ="https://i.imgur.com/Nt5DFGP.png"/>

## Cheat Sheet
- [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

- Path command is useful
- grep is useful