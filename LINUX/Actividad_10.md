# Job Control
In the previous lesson, we looked at some of the implications of Linux being a multi-user operating system. In this lesson, we will examine the multitasking nature of Linux, and how it is controlled with the command line interface.

As with any multitasking operating system, Linux executes multiple, simultaneous processes. Well, they appear simultaneous, anyway. Actually, a single processor core can only execute one process at a time but the Linux kernel manages to give each process its turn at the processor and each appears to be running at the same time.

There are several commands that are used to control processes. They are:

- ps - list the processes running on the system
- kill - send a signal to one or more processes (usually to "kill" a process)
- jobs - an alternate way of listing your own processes
- bg - put a process in the background
- fg - put a process in the foreground
## A Practical Example
While it may seem that this subject is rather obscure, it can be very practical for the average user who mostly works with the graphical user interface. Though it might not be apparent, most (if not all) graphical programs can be launched from the command line. Here's an example: there is a small program supplied with the X Window system called xload which displays a graph representing system load. We can execute this program by typing the following:
# Putting a Program into the Background
Now, in order to make life a little easier, we are going to launch the xload program again, but this time we will put it in the background so that the prompt will return. To do this, we execute xload like this:

# Listing Running Processes
Now that we have a process in the background, it would be helpful to display a list of the processes we have launched. To do this, we can use either the jobs command or the more powerful ps command.

# Killing a Process
Suppose that we have a program that becomes unresponsive; how do we get rid of it? We use the kill command, of course. Let's try this out on xload. First, we need to identify the process we want to kill. We can use either jobs or ps, to do this. If we use jobs we will get back a job number. With ps, we are given a process id (PID). We will do it both ways:

# A Little More About kill
While the kill command is used to "kill" processes, its real purpose is to send signals to processes. Most of the time the signal is intended to tell the process to go away, but there is more to it than that. Programs (if they are properly written) listen for signals from the operating system and respond to them, most often to allow some graceful method of terminating. For example, a text editor might listen for any signal that indicates that the user is logging off, or that the computer is shutting down. When it receives this signal, it could save the work in progress before it exits. The kill command can send a variety of signals to processes. Typing:
