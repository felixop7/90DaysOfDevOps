# Day 5: Advanced Linux Shell Scripting for DevOps Engineers with User Management 🐧

## Daily Log

**Date:** June 23, 2024

Today, I continued my 90 Days of DevOps journey by delving into advanced Linux shell scripting and user management. Shell scripting is a powerful tool for automating tasks, managing resources, and performing operations in an operating system, making it an essential skill for DevOps engineers.

## Key Concepts

### What is Kernel

The kernel is a computer program that is the core of a computer's operating system, with complete control over everything in the system.

### What is Shell

A shell is a special user program which provides an interface for the user to use operating system services. Shell accepts human-readable commands from the user and converts them into something which the kernel can understand. It is a command language interpreter that executes commands read from input devices such as keyboards or from files. The shell gets started when the user logs in or starts the terminal.

### What is Linux Shell Scripting?

A shell script is a computer program designed to be run by a Linux shell, a command-line interpreter. The various dialects of shell scripts are considered to be scripting languages. Typical operations performed by shell scripts include file manipulation, program execution, and printing text.

## Tasks

### Task 1: Create Directories Using a Shell Script

To create a shell script that generates directories with dynamic names based on the provided arguments, you can use the following script:
#!/bin/bash

# Check if the correct number of arguments is provided

    if [ "$#" -ne 3 ]; then
        echo "Usage: $0 <directory_name> <start_number> <end_number>"
        exit 1
    fi

# Assign command-line arguments to variables

    directory_name=$1
    start_number=$2
    end_number=$3

# Loop to create directories with dynamic names

    for ((i=start_number; i<=end_number; i++)); do
        mkdir "${directory_name}${i}"
    done

    echo "The directories have been successfully created"

Save this script as `createDirectories.sh`. You can run it with the following command:

    ./createDirectories.sh day 1 90

This will create directories named `day1`, `day2`, ..., `day90`.

### Task 2: Backup Script

Here is a simple backup script that copies all files from a source directory to a destination directory:
#!/bin/bash

# Define source and destination directories

    SOURCE_DIR="/path/to/source"
    DEST_DIR="/path/to/destination"

# Create a backup

    cp -r "$SOURCE_DIR" "$DEST_DIR"

    echo "Backup completed successfully"

    Save this script as `backup.sh`. You can run it with the following command:
    ./backup.sh

### Task 3: Automate Backup Script with Cron

To automate the backup script using cron, you need to edit the crontab file:
Open the crontab file for editing:

    crontab -e

Add the following line to schedule the backup script to run daily at midnight:

    0 0 * * * /path/to/backup.sh

This will ensure that the backup script runs every day at midnight.

### Task 4: User Management

To create two users and display their usernames, you can use the following commands:

# Create users

    sudo useradd user1
    sudo useradd user2

# Display usernames

    echo "Created users:"
    echo "user1"
    echo "user2"

This will create two users named `user1` and `user2` and display their usernames.

## Reflection

Shell scripting and user management are powerful tools in the hands of a DevOps engineer. It was challenging to learn, but I'm excited about the possibilities it opens up for automation and system management. I'm looking forward to continuing my journey in the #90DaysOfDevOps challenge!

## References

- [Advanced Linux Shell Scripting for DevOps Engineers with User Management](https://www.youtube.com/watch?v=39oyFIStuaI)
- [EASIEST Shell Scripting Tutorial for DevOps Engineers](https://www.youtube.com/watch?v=39oyFIStuaI)
- [Linux For DevOps - Masterclass by Shubham Londhe](https://www.youtube.com/live/P90wg2SfpzM)
- [GeeksForGeek- User Management in Linux](https://www.geeksforgeeks.org/user-management-in-linux/)

---

Happy Learning! 🚀

**Roshan Sahani**
