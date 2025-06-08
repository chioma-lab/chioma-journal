# CLI (Command Line Interface) Overview

The terminal is the black screen that appears when you search for “terminal” on your computer. It provides direct access to the system kernel—the core of your operating system—and allows you to interact with your computer through text commands.

Learning how to use the terminal is useful for everyone, not just programmers.

For programmers, it's essential for navigating systems efficiently, running scripts, managing files, and using tools like Git.

For **non-programmers**, it builds confidence in managing tasks like file organization, troubleshooting, and automation. You get to understand what's happening behind the scenes and take more control of your device.

One key thing to note is that the terminal responds only to correct commands—there's no guesswork. The more you practice, the more intuitive it becomes.


---

## Getting Started with the CLI

Here’s a step-by-step guide to help you start using the Command Line Interface, especially if you’re new to it.

### Step 1: Launch the Terminal

- On **Linux** or **macOS**, search for and open **Terminal**.
- On **Windows**, use **Windows Subsystem for Linux (WSL)** or tools like **Git Bash**.

For WSL users, type `wsl` in the search bar and launch.

### Step 2: Understand the Shell Prompt

Example prompt:
```
chioma-lab@DESKTOP-XXX:~$
```
- `chioma-lab`: username
- `DESKTOP-XXX`: hostname
- `~`: home directory
- `$`: regular user indicator

### Step 3: Know Where You Are
```bash
pwd
```
Example output:
```bash
/home/chioma-lab
```

### Step 4: List Contents in Your Directory
```bash
ls
ls -la
```

### Step 5: Move Around Using `cd`
```bash
cd folder-name
cd ..      # up one level
cd ~       # home directory
```

### Step 6: Create Folders and Files
```bash
mkdir new_folder
touch newfile.txt
```

### Step 7: View File Types and Contents
```bash
file newfile.txt
less newfile.txt
```

### Step 8: Copy, Move, and Delete
```bash
cp source.txt destination.txt
mv oldname.txt newname.txt
rm filename.txt
rm -r folder-name
```

### Step 9: Understand Wildcards and Patterns
```bash
cp *.txt backup/
```
This copies all `.txt` files into the backup folder.

### Step 10: Use Help and Manuals
```bash
man ls
ls --help
```

---

## Practice Task

Using the above knowledge, perform the following:

Create the following directory structure under a folder named `Linux_navigation`, each with a `.gitkeep` file as a placeholder:

- `new_school`
- `right_school`
- `temp`
- `not_here`
- `school_is_amazing`

**Commands involved:** `mkdir`, `touch`, `cd`, `ls`, `pwd`

**Example output:**
```bash
Linux_navigation/
├── new_school/
│   └── .gitkeep
├── right_school/
│   └── .gitkeep
├── temp/
│   └── .gitkeep
├── not_here/
│   └── .gitkeep
├── school_is_amazing/
    └── .gitkeep
```

---

## Practice Tasks and Learning

Task 1: View Working Directory

```
pwd
```

Output:

```
mnt/c/Users/me
```

Note: wsl entry point

Task 2: Change Directory to Home

```
cd
```

Output

```
home/me
```

Task 3: Create and Navigate Directories

```
mkdir school
cd school
pwd
```

Output:

```
home/me/school
```

Task 4: Create Subdirectories

```
mkdir right_school
cd right_school
pwd
```

Output:

```
home/me/school/right_school
```

Task 5: Use Relative Path to Navigate Up

```
cd ..
pwd
```

Output:

```
home/me/school
```

Task 6: Use Absolute Path to Go to the Home Directory

```
cd home/me
pwd
```

Output:

```
home/me
```

Task 7: List Files

```
ls
```

Output:

```
school
```

Task 8: List Files and View Hidden Files

```
ls -a
```

Output:

```
.  ..  .bashrc  .profile  school
```

Task 9: Use --help and man to Understand a Command

```
ls --help
```

This gives a quick view of what ls does and how to use it.

```
man ls
```

This gives a detailed manual on how to use the ls command.


#### Author: 

Chioma Williams  

**Email:** chiomawilliams001@gmail.com

