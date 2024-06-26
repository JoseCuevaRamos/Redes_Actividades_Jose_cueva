# I/O Redirection
In this lesson, we will explore a powerful feature used by command line programs called input/output redirection. As we have seen, many commands such as ls print their output on the display. This does not have to be the case, however. By using some special notations we can redirect the output of many commands to files, devices, and even to the input of other commands.

# Standard Output
Most command line programs that display their results do so by sending their results to a facility called standard output. By default, standard output directs its contents to the display. To redirect standard output to a file, the ">" character is used like this:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/d3d6fee9-1900-48e5-96a0-bef8f6d35f77)
![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/494beead-a20a-41ed-bd10-dd700216361a)


In this example, the ls command is executed and the results are written in a file named file_list.txt. Since the output of ls was redirected to the file, no results appear on the display.

Each time the command above is repeated, file_list.txt is overwritten from the beginning with the output of the command ls. To have the new results appended to the file instead, we use ">>" 
# Standard Input
Many commands can accept input from a facility called standard input. By default, standard input gets its contents from the keyboard, but like standard output, it can be redirected. To redirect standard input from a file instead of the keyboard, the "<" character is used like this:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/cff48647-79d6-4292-a664-77d1b5104f84)


# Pipelines
The most useful and powerful thing we can do with I/O redirection is to connect multiple commands together to form what are called pipelines. With pipelines, the standard output of one command is fed into the standard input of another. Here is a very useful example:

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/8961d885-434b-4c3f-afb4-52b44663a6de)

