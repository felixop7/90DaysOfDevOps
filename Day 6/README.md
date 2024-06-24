# Day 6: File Permissions and Access Control Lists 🐧

## Daily Log

**Date:** June 24, 2024

Today, I continued my 90 Days of DevOps journey by learning about file permissions and Access Control Lists (ACLs) in Linux. Understanding file permissions and ACLs is crucial for managing access to files on a Linux system.

## Key Concepts

### Linux File Permissions

In Linux, each file and directory has a set of permissions associated with it, which specifies who can read, write, or execute the file or directory. These permissions are divided into three categories:

- **Owner** — The owner of the file or application. The `chown` command is used to change the ownership permission of a file or directory.
- **Group** — The group that owns the file or application. The `chgrp` command is used to change the group permission of a file or directory.
- **Others** — All users with access to the system. The `chmod` command is used to change the other users permissions of a file or directory.

### Access Control Lists (ACLs)

ACLs provide a more flexible permission mechanism than traditional Linux file permissions. They allow you to specify permissions for individual users and groups, and even for multiple users and groups.

## Tasks

### Task 1: Create a simple file and change its permissions

To create a simple file and change its permissions, you can use the following commands:

    touch myfile
    ls -ltr myfile
    chmod 755 myfile
    ls -ltr myfile

This will create a file named `myfile`, display its permissions, change its permissions to `755` (read, write, and execute permissions for the owner, and read and execute permissions for the group and others), and display the updated permissions.

### Task 2: Write an article about File Permissions

System security is a major concern for any system administrator or DevOps professional. In a multi-user environment, it is crucial to maintain strict control over which users have access to specific files and directories and what actions they can perform on those resources. This is where Linux file permissions come into play.

The Linux operating system provides a robust and flexible system for managing user permissions and access control. Each file and directory within a Linux system has a set of associated permissions that dictate who can read, write, or execute it. These permissions are divided into three categories:

    Owner: The owner of the file or application. The chown command is used to change the ownership permission of a file or directory.
    Group: The group that owns the file or application. The chgrp command is used to change the group permission of a file or directory.
    Others: All users with access to the system, outside of the owner and group. The chmod command is used to change the other users permissions of a file or directory.

When you list files in a directory using the ls -l command, you'll see the permissions for each file and directory represented by a string of 10 characters, like this: -rw-rw-r--.

The first character refers to the type of file (- for a regular file, d for a directory). The next nine characters are split into three sets of three characters each, representing the permissions for the owner, group, and others, respectively. Each set can include the following characters:

    r: The file is readable.
    w: The file is writable.
    x: The file is executable.
    -: The indicated permission is not granted.

For instance, in our example -rw-rw-r--, the owner has read and write permissions (rw-), the group also has read and write permissions (rw-), and others only have read permissions (r--).

Changing permissions is done using the chmod command, which can operate in symbolic mode (using r, w, x to represent permissions) or absolute mode (using numbers to represent permissions: 4 for read, 2 for write, 1 for execute). For example, to give the owner read, write, and execute permissions, and only read permissions to the group and others, you could use either chmod u=rwx,g=r,o=r filename (symbolic mode) or chmod 744 filename (absolute mode).

While this system of permissions can handle many common use cases, it has limitations. For instance, it does not allow you to set permissions for individual users outside of the owner, or multiple groups. This is where Access Control Lists (ACLs) come in.
ACLs provide a more granular level of control over file permissions. They allow you to set permissions for specific users and groups, using the setfacl command to set the ACLs and getfacl to view them. For example, to give the user john read and write access to a file, you could use setfacl -m u:john:rw filename.

In conclusion, understanding and properly managing file permissions and ACLs is a fundamental part of maintaining security in a Linux environment. By carefully assigning permissions, DevOps professionals can ensure that each user only has access to the files they need, and can only perform necessary actions on those files, protecting the system from accidental damage or malicious activity.

### Task 3: Read about ACL and try out the commands `getfacl` and `setfacl`

ACLs are a way of assigning finer-grained permissions to files and directories in Linux. The `getfacl` command displays the ACLs for a file or directory, and the `setfacl` command sets the ACLs. For example, to give the user `john` read and write access to a file named `myfile`, you could use the following command:

    setfacl -m u:john:rw myfile

And to display the updated ACLs, you could use the following command:

    getfacl myfile

### Task 4: Read about User Management

User management involves creating, deleting, and managing users on a Linux system. This is crucial for maintaining the security of a system, as each user should have the minimum necessary permissions to perform their tasks. For example, a regular user should not have root permissions, as they could accidentally or intentionally damage the system.

## Reflection

Understanding file permissions and ACLs is crucial for managing access to files on a Linux system. By correctly setting these permissions, you can ensure that only authorized users have access to sensitive files. I'm looking forward to continuing my journey in the #90DaysOfDevOps challenge!

## References

- [Linux*Basic*&\_FilePermissions](Linux_Basic_&_FilePermissions.docx)

---

Happy Learning! 🚀

**Roshan Sahani**
