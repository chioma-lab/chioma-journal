# Navigating The Linux System

Linux is a family of open-source, Unix-like operating systems that all share the Linux kernel as their foundation.

Linux, being open-source is free to modify and distribute, this led to the emergence of various Unix-like operating systems known as **distributions** (***or distros***) such as *Fedora*, *Debian* and most popular beginners' friendly which is ***Ubuntu***, a distro I am currently interacting with.

Linux CLI (*Command Line Interface*) unlike GUIs (*Graphical User Interfaces*) allows for complex files manipulations through the Bash shell using commands like `pwd`, `cd`, `ls` (*the basics*) etc.

---

## The Linux File System

Similar to the Windows file system, the Linux file system is organized in a tree-like structure. However, it does not employ the concept of ***Drive Letters*** where each storage device is assigned an alphabetical letter to indicate a stand-alone tree. In a Linux file system, a hierarchical tree is maintained, with `/` (*the root*) representing the top-most directory. All other files and directories branch out from this root, including those from different storage devices, which are mounted within the  structure. For example, in the context of WSL (*Windows Subsystem for Linux*), a mounted device would be:

Syntax
 `/mnt/c/Users/Me`

Actual Example
`/mnt/c/Users/Chioma

This is a virtual integration of my  Windows local drive assigned the alpahbetical letter `C:` into the environment of a WSL (Linux) file system (single) tree.

#### Breakdown

`/mnt`: A common directory for mounting external or additional file system.
`/c`: C: drive from Windows mounted on WSL.
`/mnt/c/Users/Chioma`: My specified User folder on Windows, accessible through WSL.

---

## Task

Navigate the Linux file system using basic tools like `cd, touch, cp, mv, rm, mkdir, an option -r`

### Task Outcome

By the end of the task, I should have:

- Directories named "new_school", right_school", "temp", "not_here", "school_is_amazing", with placeholder files in each named ".gitkeep" all in my "Linux_navigation" directory which will serve the root directory in this context.

---

## Giving Context To Basic Linux Concepts and Features

- **pwd**: Print Working Directory. A command you run on the CLI to know your working directory.

Generic Example
`

<span style="green">me@machine:WD$</span> pwd
<span style="green">/home/me<span/>

`

Actual Example
`

<span style="green">chioma-lab@DESKTOP-XXX:~$</span> pwd
<span style="green">/home/chioma-lab</span>

`

#### Breakdown

`<span style="green">chioma-lab@DESKTOP-XXX~$</span>` is a representation of the Bash shell prompt in Linux subsystem.

Where:

`<span style="green">chioma-lab</span>`: The **username** currently logged into the subsystem
`<span style="green">DESKTOPXXX</span>`: The **hostname** of the machine, in this case, my Windows pc.
`<span style="green">~</span>`: Tilde represents the **home directory** of the current user (shorthand for `<span style="green">/home/chioma-lab`</span>). This part of the Bash shell prompt is **dynamic** as it changes when the **working directory** thus shown as **WD** (although, WD is not literally shown as a component of Bash shell, treat as an illustration)
`<span style="green">$</span>`: Indicates I am an **ordinary user**. Not a **root** user. A **root** user would see **#** instead,

Hence, the bash shell prompt:

`<span style="green">chioma-lab@DESKTOP-XXX:~$</span>`

I am logged in as an ordinary user as `chioma-lab` in my home directory using bash via wsl on a host machine named `<span style="green">DESKTOP-XXX</span>`.

- **Working** Directory: The current directory you're operating from in the CLI.
- **Directory**: Known as "folder" in the Windows file system.
- **Root Directory**: Represented as `/` in the Linux file system. The top-most layer that houses everything in the linux file system. See it as the starting point of your file system. When you whip up your Linux system you're typically taken to your home directory by default. Folders you can find here `/home, /bin, /etc, /var`, etc.
- **Home Directory**: Can be represented as `~`. It is a system subdirectory `/home` in the the root directory to house various users' accounts. Can be considered as your login shell starting point for a user. Configuration files like `.bashrc` are usually found here. 
- **Pathname**: The route taken along the branches of the tree to get to the desired ***working directory***. See it as an address to desired resources. An example of a pathname:
`/home/chioma-lab/Alx-Learning-Journal`.
Pathname can be **Absolute or Relative**
	- Absolute Pathname: Starts from the root directory and works its way along the branches until the path to the desired directory is complete.
	- Relative Pathname: Works its way from the working directory to the desired directory.
- **Linux Shell Prompt**: Shows readiness to take instruction. The shell prompt typically changes to the working directory.
- **Bash Shell Prompt**: The default shell in most linux distros. The Bash prompt typically end with `$` for regular users and `#` for root users.
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

Crucial Tools In Interacting With Linux System

| Tool | Options | Construction | Function |
|:---|:---|:---|:---|
| ls | | | List files in the working directories |
| ls | | ls /bin | List files in the specified directory `/bin` |
| ls | -l | ls -l | List all files in the working directory in a long format |
| ls | -l | ls -l /etc /bin | List all files in the directory /`etc` and `/bin` in a long format |
| ls | -la | ls -la .. | List all files both the hidden folders of the working directory parent's directory in a long format|
| cp | | Copy files and directory |
| mv | | Move or rename files and directories |
| rm | | Remove files and directories |
| mkdir | | Create directory | 


By: Chioma Williams
Email: chiomawilliams001@gmail.com
