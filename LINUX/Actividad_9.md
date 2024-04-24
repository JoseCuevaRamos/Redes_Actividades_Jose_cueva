# Permissions
The Unix-like operating systems, such as Linux differ from other computing systems in that they are not only multitasking but also multi-user.

What exactly does this mean? It means that more than one user can be operating the computer at the same time. While a desktop or laptop computer only has one keyboard and monitor, it can still be used by more than one user. For example, if the computer is attached to a network, or the Internet, remote users can log in via ssh (secure shell) and operate the computer. In fact, remote users can execute graphical applications and have the output displayed on a remote computer. The X Window system supports this.

The multi-user capability of Unix-like systems is a feature that is deeply ingrained into the design of the operating system. If we remember the environment in which Unix was created, this makes perfect sense. Years ago before computers were "personal," they were large, expensive, and centralized. A typical university computer system consisted of a large mainframe computer located in some building on campus and terminals were located throughout the campus, each connected to the large central computer. The computer would support many users at the same time.

In order to make this practical, a method had to be devised to protect the users from each other. After all, we wouldn't want the actions of one user to crash the computer, nor would we allow one user to interfere with the files belonging to another user.

This lesson will cover the following commands:

- chmod - modify file access rights
- su - temporarily become the superuser
- sudo - temporarily become the superuser
- chown - change file ownership
- chgrp - change a file's group ownership

# File Permissions
On a Linux system, each file and directory is assigned access rights for the owner of the file, the members of a group of related users, and everybody else. Rights can be assigned to read a file, to write a file, and to execute a file (i.e., run the file as a program).

To see the permission settings for a file, we can use the ls command. As an example, we will look at the bash program which is located in the /bin directory:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/be0e7626-681e-4e6a-b5f9-5e809718732c)


# chmod
The chmod command is used to change the permissions of a file or directory. To use it, we specify the desired permission settings and the file or files that we wish to modify. There are two ways to specify the permissions. In this lesson we will focus on one of these, called the octal notation method.

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/cb47e872-cb81-4054-916e-cd5c232081ee)


It is easy to think of the permission settings as a series of bits (which is how the computer thinks about them)
# Directory Permissions
The chmod command can also be used to control the access permissions for directories. Again, we can use the octal notation to set permissions, but the meaning of the r, w, and x attributes is different:

- r - Allows the contents of the directory to be listed if the x attribute is also set.
- w - Allows files within the directory to be created, deleted, or renamed if the x attribute is also set.
- x - Allows a directory to be entered (i.e. cd dir).
Here are some useful settings for directories:

# Becoming the Superuser for a Short While
It is often necessary to become the superuser to perform important system administration tasks, but as we know, we should not stay logged in as the superuser. In most distributions, there is a program that can give you temporary access to the superuser's privileges. This program is called su (short for substitute user) and can be used in those cases when you need to be the superuser for a small number of tasks. To become the superuser, simply type the su command. You will be prompted for the superuser's password:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/e9208430-a22d-4f70-aa26-297101451b39)


![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/0901e9de-bff5-4c6e-a468-67a3b341fa4b)


# Changing File Ownership
We can change the owner of a file by using the chown command. Here's an example: Suppose we wanted to change the owner of some_file from "me" to "you". We could:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/e869485c-d02e-4c38-8f3f-eff15c8cec14)


