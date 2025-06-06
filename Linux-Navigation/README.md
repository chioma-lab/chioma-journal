# Navigating The Linux System

Linux is a family of open-source Unix-like system with the most popular version based on the linux kernel.

Since Linux is open-source are free to modification and distribution, this emerged various versions of the Linux system known as __Distros__ (*Distributions*) such as *Fedora*, *Debian* and most popular beginner friendly which is ***Ubuntu***, a distro I am curently interacting with.

The linux unlike GUIs is CL-based and files are manipulated and shell navigated using programs like `pwd`, `cd`, `ls` (*the basics*) etc.
---
## The Linux File System

Similar to the Windows file system, the Linux file system is organized in a tree-like structure. However, it does not employ the concept of ***Drive Letters*** where each storage device is assigned an alphabethical letter to indicate a seperate tree. In a Linux file system, a tree is maintained which is the top-layer of the file structure but may branch out to incate different storages.
---
## Task

Navigate the Linux file system using basic tools like `cd, touch, cp, mv, rm, mkdir, an option -r`

### Task Outcome

By the end of the task, I should have:

- Directories named "new_school", right_school", "temp", "not_here", "school_is_amazing", with placeholder files in each named ".gitkeep" all in my "Linux_navigation" directory which will serve the root directory in this context.
---
## Giving Context To Basic Linux Concepts and Features

- **PWD**:A program you run on your cli to know your working directory.
- **Working** Directory: The directory in which you're in.
- **Directory**: Known as "folder" in the Windows file system.
- **Root Directory**: Represented as `/` in the Linux file system.The top-most layer that houses everything in the linux file system.See it as the startingpoint of your file system. When you whip up your Linux system you're typically taken to your home directory by default. Folders you can find here `/home, /bin, /etc, /var`, etc.
- **Home Directory**:Can be represented as `~`. It is a system subdirectory `/home` in the the root directory to house various users' accounts. Can be considered as your login shell starting point for a user. Configuration files like `.bashrc` are usually found here. 
- **Pathname**: The root take along the branches of the tree to get to the desired ***working directory***. See it as an address to a resources. An example of a pathname:
`/home/chioma-lab/Alx-Learning-Journal`.
Pathname can be **Absolute or Relative**
	- Absolute Pathname: Starts from the root directory and works its way along the branch until the path to the desired directory is complete.
	- Relative Pathname: Works its way the working directory to the desired directory.
- **Linux Shell Prompt**: Shows readiness to take instruction. The shell prompt typically changes to the working directory.
- **Bash Shell Prompt**: 
- **Special Notations**: In the context of file navigation.
	- `.`: Indicates the working directory itself.
	- `..`: The working directory parent's directory.
- **Options**: They are programs the adds more behavior to the linux commands. An example:
 ```
# List all content in the specified directory both the ones that start with period (hidden files) in a long format.

Syntax: ls -la /Alx-Learning-Journal

```
Others,`-i` to interact with a file before command exection and `-r` to perform an action recursively.

- **ASCII**: The mapping of text to numbers. An American standardization encoding scheme for text representation.
- **Text**: A simple one-to-one mapping of characters to numbers.
- **less**: A program that once invoked, allows us to view text files.
`less text_file`
- **file**: Helps determine what type of file it is before viewing. Some file types are bash, html, jpeg etc.

`file name-of-file`
- `*`: Symbolizes a ***Wild card***. A command line feature that allows complex file manipulatins through the concept of special characters to rapidly specify groups of filenames based on patterns. 
[Wildcard Cheat Sheet](./wildcard_cheatsheet.md)

```
cp -u *.html destination

# Copy only updated files that ends in the specified extension to the destination folder

```
---
## Crucial Tools In Interacting With Linux System

| Tool | Options | Function |
|:---|:---|:---|
| ls | | List files in the working directories |
| ls /bin | | List files in the specified directory |
| ls -l | -l | List all files in the working directory in the long format |
| ls -l /etc /bin | -l | List all files in the directory etc and bin in a long format |
| ls -la .. | -la | List all files both the hidden folders of the working directory parent's directory in a long format|
| cp | | Copy files and directory |
| mv | | Move or rename files and directories |
| rm | | Remove files and directories |
| mkdir | | Create directory | 

