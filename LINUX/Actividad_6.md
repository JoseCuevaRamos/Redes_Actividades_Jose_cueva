# Working with Commands
Up until now, we have seen a number of commands and their mysterious options and arguments. In this lesson, we will try to remove some of that mystery. We will introduce the following commands.

- type - Display information about command type
- which - Locate a command
- help - Display reference page for shell builtin
- man - Display an on-line command reference
# What are "Commands?"
## Commands can be one of 4 different kinds:

1. An executable program like all those files we saw in /usr/bin. Within this category, programs can be compiled binaries such as programs written in C and C++, or programs written in scripting languages such as the shell, Perl, Python, Ruby, etc.
2. A command built into the shell itself. bash provides a number of commands internally called shell builtins. The cd command, for example, is a shell builtin.
3. A shell function. These are miniature shell scripts incorporated into the environment. We will cover configuring the environment and writing shell functions in later lessons, but for now, just be aware that they exist.
4. An alias. Commands that we can define ourselves, built from other commands. This will be covered in a later lesson.
## Identifying Commands
It is often useful to know exactly which of the four kinds of commands is being used and Linux provides a couple of ways to find out.

# type
The type command is a shell builtin that displays the kind of command the shell will execute, given a particular command name. It works like this:
# which
Sometimes there is more than one version of an executable program installed on a system. While this is not very common on desktop systems, it's not unusual on large servers. To determine the exact location of a given executable, the which command is used:
# Getting Command Documentation
With this knowledge of what a command is, we can now search for the documentation available for each kind of command.

# help
bash has a built-in help facility available for each of the shell builtins. To use it, type “help” followed by the name of the shell builtin. Optionally, we can add the -m option to change the format of the output. For example:
# --help
Many executable programs support a “--help” option that displays a description of the command's supported syntax and options. For example:
# man
Most executable programs intended for command line use provide a formal piece of documentation called a manual or man page. A special paging program called man is used to view them. It is used like this:
