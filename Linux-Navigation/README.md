# Understanding The Linux System

Developing the knowledge of manipulating files and navigating the Bash shell using text commands is a powerful skill—not just for programmers, but also for non-programmers. In this lesson, you'll be introduced to the basics to help you start interacting with a traditional Linux system or a subsystem like WSL. For illustration purposes, this lesson references WSL. To reinforce your learning, I've curated practical tasks for you to explore. Let’s get started!

Linux is a family of open-source, Unix-like operating systems that all share the Linux kernel as their foundation.

Linux, being open-source is free to modify and distribute, this led to the emergence of various Unix-like operating systems known as **distributions** (***or distros***) such as *Fedora*, *Debian* and most popular beginners' friendly which is ***Ubuntu***, a distro I am currently interacting with.

Linux CLI (*Command Line Interface*) unlike GUIs (*Graphical User Interfaces*) allows for complex files manipulations through the shell (***Bash***) using commands like `pwd`, `cd`, [ls](https://linuxcommand.org/lc3_man_pages/ls1.html) (*the basics*) etc.

---

## The Linux File System

Similar to the Windows file system, the Linux file system is organized in a tree-like structure. However, it does not employ the concept of ***Drive Letters*** where each storage device is assigned an alphabetical letter to indicate a stand-alone tree. In a Linux file system, a hierarchical tree is maintained, with `/` (*the root*) representing the top-most directory. All other files and directories branch out from this root, including those from different storage devices, which are mounted within the  structure. For example, in the context of WSL (*Windows Subsystem for Linux*), a mounted device would be:

Syntax

 ```
/mnt/c/Users/Me
```

Actual Example

```
/mnt/c/Users/Chioma
```

This is a virtual integration of my  Windows local drive assigned the alpahbetical letter `C:` into the environment of a WSL (Linux) file system (single) tree.

#### Breakdown

`/mnt`: A common directory for mounting external or additional file system.

`/c`: C: drive from Windows mounted on WSL.

`/mnt/c/Users/Chioma`: My specified User folder on Windows, accessible through WSL.

---

## Giving Context To Basic Linux Concepts and Features

- `pwd`: Print Working Directory. A command you run on the CLI to know your working directory.

Generic Example
```
me@machine:WD$ pwd
/home/me
```

Actual Example
```
chioma-lab@DESKTOP-XXX:~$ pwd
/home/chioma-lab
```

#### Breakdown

`chioma-lab@DESKTOP-XXX~$` is a representation of the Bash prompt in Linux subsystem.

Where:

`chioma-lab`: The **username** currently logged into the subsystem.

`DESKTOPXXX`: The **hostname** of the machine, in this case, my Windows pc.

`~`: Tilde represents the **home directory** of the current user (shorthand for `/home/chioma-lab`). This part of the Bash prompt is **dynamic** as it changes when the **working directory** does shown as **WD** (although, WD is not literally shown as a component of Bash shell, treat as an illustration).

`$`: Indicates I am an **ordinary user**. Not a **root** user. A **root** user would see `#` instead,

Hence, the bash prompt:

```
chioma-lab@DESKTOP-XXX:~$
```

I am logged in as an ordinary user as `chioma-lab` in my home directory using bash via wsl on a host machine named `DESKTOP-XXX`.

- **Working** Directory: The current directory you're operating from in the CLI. You use the `pwd` command to print your working directory

Example:

```
me@machine:~$ pwd
/home/me
```

- **Directory**: Known as "folder" in the Windows file system.
- **Root Directory**: Represented as `/` in the Linux file system. The top-most layer that houses everything in the linux file system. See it as the starting point of your file system. When you whip up your Linux system you're typically taken to your home directory by default. Folders you can find here `/home, /bin, /etc, /var`, etc.
- **Home Directory**: Can be represented as `~`. It is a system subdirectory `/home` in the the root directory to house various users' accounts. Can be considered as your login shell starting point for a user. Configuration files like `.bashrc` are usually found here. When you leave your home directory, you can retun to it with the command `cd` followed by no argument.

```
me@machine:~$ cd
pwd
home/me
```
- **Argument**: Used to customize the actions of a command. They can specify input files, output locations, options, or other parameters. Arguments are typically entered after the command name, separated by spaces. Arguments can be filenames, text strings, numbers, or other objects. The filename argument type is most popular amongst non-programmers.
- **Pathname**: The route taken along the branches of the tree to get to the desired ***working directory***. See it as an address to desired resources.
Pathname can be **Absolute or Relative**
	- Absolute Pathname: Starts from the root directory and works its way along the branches until the path to the desired directory is complete.

Example:

```
/home/me/path/to/a/filename
```

	- /*Relative Pathname: Works its way from the working directory to the desired directory.

Example:

```
./path/to/a/desired_directory
```
- **Linux Shell Prompt**: Shows readiness to take instruction. The shell prompt typically changes to the working directory.
- **Bash Prompt**: The default shell in most linux distros. The Bash prompt typically end with `$` for regular users and `#` for root users.
- **Special Notations**: In the context of file navigation.
	- `.`: Indicates the working directory itself.
	- `..`: The working directory parent's directory.
- **Options**: They are programs the adds more behavior to the linux commands.

Example:

```
ls -la
```

Lists all content in a specified directory both the ones that start with period (hidden files) in a long format.

Others,`-i` to interact with a file before command exection and `-r` to perform an action recursively.

- **ASCII**: The mapping of text to numbers. An American standardization encoding scheme for text representation.
- **Text**: A simple one-to-one mapping of characters to numbers. You use the less command to view text files.
- **less**: [less](https://linuxcommand.org/lc3_man_pages/less1.html) program that once invoked, allows us to view text files and [navigate](./Controlling_Less.md) through the pages.

Example:

```
less text_file
```
- **file**: Helps determine what [type of file](./File_Types.md) it is before viewing. Some file types are bash, html, jpeg etc.

`file name-of-file`
- `*`: /*Symbolizes a ***Wild card***. A command line feature that allows complex file manipulations through the concept of special characters to rapidly specify groups of filenames based on patterns. 
[Wildcard Cheat Sheet](./wildcard_cheatsheet.md). 

Optional: [Deeper dive into wildcard](./Wildcard_Advance.md)

```
cp -u *.html destination

# Copy only updated files that ends in the specified extension to the destination folder

```
---

Crucial Tools In Interacting With Linux System

| Tool | Options/flag | Construction | Function |
|:---|:---|:---|:---|
| ls | | | List files in the working directories |
| ls | | ls /bin | List files in the specified directory `/bin` |
| ls | -l | ls -l | List all files in the working directory in a long format |
| ls | -l | ls -l /etc /bin | List all files in the directory /`etc` and `/bin` in a long format |
| ls | -la | ls -la .. | List all files both the hidden folders of the working directory parent's directory in a long format|
| cp | | | Copy files and directory |
| mv | | | Move or rename files and directories |
| rm | | | Remove files and directories |
| mkdir | | | Create directory |
| --help| Used after a command | ls --help | Shows quick help for a command |
| man | | man ls | Displays manual or detailed usage of a command |

## Task

Navigate the Linux file system using basic tools like cd, touch, [cp](https://linuxcommand.org/lc3_man_pages/cp1.html), [mv](https://linuxcommand.org/lc3_man_pages/mv1.html), [rm](https://linuxcommand.org/lc3_man_pages/rm1.html), [mkdir](https://linuxcommand.org/lc3_man_pages/mkdir1.html), an option `-r`

### Task Outcome

By the end of the task, you should have:

- Directories named "new_school", right_school", "temp", "not_here", "school_is_amazing", with placeholder files in each named ".gitkeep" all in my "Linux_navigation" directory which will serve the root directory in this context.

Click [here](./Practice_Task.md) for a step-by-step getting started with CLI, and a practice along tasks if you feel unsure.

[Further Reading](https://tldp.org/LDP/Linux-Filesystem-Hierarchy/html/tmp.html)

#### Author:

Chioma Williams

**Email**: chiomawilliams001@gmail.com
