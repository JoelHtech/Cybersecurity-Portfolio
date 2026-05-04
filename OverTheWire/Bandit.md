# Write-Up for the Bandit Wargame

## Bandit 0 – Log into the game using SSH

The objective of this level is to log into the Bandit wargame using SSH.

The following credentials were provided:

* Host: `bandit.labs.overthewire.org`
* Port: `2220`
* Username: `bandit0`
* Password: `bandit0`

To connect to the server, I used the following command:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

After entering the password (`bandit0`) when prompted, I successfully logged into the system and completed Level 0.

<img width="579" height="512" alt="image" src="https://github.com/user-attachments/assets/4b4f36f7-d382-4686-aea0-8a675b8e6f08" />

### Key Concepts

* SSH (Secure Shell) for remote access.
  *   SSH is commonly used in penetration testing for remote system access.
* Basic command-line usage.

## Bandit 01 – Find the password in the readme file

The objective of this level is to find the password stored in a file called `readme` located in the home directory.

### Step 1: List files in the directory

I listed all files in the current directory using:

```bash
ls -la
```

<img width="495" height="128" alt="image" src="https://github.com/user-attachments/assets/db298a14-9fb9-4aaa-8d99-3653eb7e7b93" />

This command displays all files and directories, including hidden files (those starting with .), in long format. The long format includes file permissions, owner, size, and last modified date.

### Step 2: Read the file contents

To view the contents of the readme file, I used:

`cat` readme

This command outputs the contents of the file to the terminal, revealing the password for the next level.

## Bandit 02 - Find the password in a different file

The objective of this level is to find the password stored in a file `-` located in the home directory.

### Step 1: List all files in the directory

I listed all files in the current directory using:

```bash
ls -la
```

<img width="499" height="134" alt="image" src="https://github.com/user-attachments/assets/c89b0615-4d77-46b1-ae98-104873c8be21" />

### Step 2: Read the file contents

When running `cat -` no output was produced, this is because `-` is treated as a **special argument**, not a normal filename.

By telling Linux explicitly that this is a file path, not an option using:

```bash
cat ./-
```

This command outputs the contents of the file to the terminal, revealing the password.

## Bandit 03 - 

