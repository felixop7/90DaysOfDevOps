# Day 4: Basic Linux Shell Scripting for DevOps Engineers 🐧

## Daily Log

**Date:** June 16, 2024

Today, I continued my 90 Days of DevOps journey by diving into basic Linux shell scripting. Shell scripting is a powerful tool for automating tasks, managing resources, and performing operations in an operating system, making it an essential skill for DevOps engineers.

## Key Concepts

### What is Kernel

The kernel is a computer program that is the core of a computer's operating system, with complete control over everything in the system.

### What is Shell

A shell is a special user program which provides an interface for the user to use operating system services. Shell accepts human-readable commands from the user and converts them into something which the kernel can understand. It is a command language interpreter that executes commands read from input devices such as keyboards or from files. The shell gets started when the user logs in or starts the terminal.

### What is Linux Shell Scripting?

A shell script is a computer program designed to be run by a Linux shell, a command-line interpreter. The various dialects of shell scripts are considered to be scripting languages. Typical operations performed by shell scripts include file manipulation, program execution, and printing text.

## Tasks

### Explain in your own words and examples, what is Shell Scripting for DevOps.

Shell scripting is the art of writing scripts (sets of commands) in a shell language to automate tasks or to interact with the operating system. In a DevOps context, shell scripts are essential for tasks such as deploying, configuring, and monitoring systems, as well as automating routine processes like backups and log management.

### What is #!/bin/bash? can we write #!/bin/sh as well?

The shebang, represented by `#!/bin/bash`, is the first line of a shell script. It tells the system which interpreter to use to execute the script. In this case, `#!/bin/bash` specifies that the Bash shell should interpret the script. Yes, we can also write `#!/bin/sh` if we want the script to be interpreted by the Bourne shell.

### Write a Shell Script which prints "I will complete #90DaysOfDevOps challenge"

    #!/bin/bash
    echo "I will complete #90DaysOfDevOps challenge"

### Write a Shell Script to take user input, input from arguments and print the variables.

    #!/bin/bash
    echo "Enter your name:"
    read name
    echo "Hello $name, you entered $1 as your first argument and $2 as your second argument."


### Write an Example of If else in Shell Scripting by comparing 2 numbers

    #!/bin/bash
    echo "Enter two numbers:"
    read num1 num2
    if [ $num1 -gt $num2 ]
    then
    echo "$num1 is greater than $num2"
    elif [ $num1 -eq $num2 ]
    then
    echo "$num1 is equal to $num2"
    else
    echo "$num1 is less than $num2"

## Reflection

Shell scripting is a powerful tool in the hands of a DevOps engineer. I'm excited about the possibilities it opens up for automation and system management. I'm looking forward to continuing my journey in the #90DaysOfDevOps challenge!

## References

- [Basic Linux Shell Scripting for DevOps Engineers](https://www.youtube.com/watch?v=39oyFIStuaI)
- [EASIEST Shell Scripting Tutorial for DevOps Engineers](https://www.youtube.com/watch?v=39oyFIStuaI)

---

Happy Learning! 🚀

**Roshan Sahani**
