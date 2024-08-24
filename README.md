<h1 align = "center">Simple Shell</h1>

![](https://user-images.githubusercontent.com/74038190/213760705-0d5bf320-4f43-4352-b74b-0889ae726bf7.gif)

## About
A simple shell is a basic command-line interpreter that allows users to interact with the operating system by executing commands. It typically supports standard operations such as running programs, handling input/output redirection, and managing processes.

## Features
- **Command Execution:** Execute standard UNIX commands alongside some custom built-ins.
- **File Navigation:** Easily navigate through directories and manage files.
- **Process Management:** Oversee and control the execution of processes.
- **Script Execution:** Run simple shell scripts to automate tasks.

## Usage

1.Compile the code:
```bash
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

2.Run the compiled shell:
```bash
./hsh
```
****
## List of allowed functions and system calls for this project
 - access (man 2 access)
 - chdir (man 2 chdir)
 - close (man 2 close)
 - closedir (man 3 closedir)
 - execve (man 2 execve)
 - exit (man 3 exit)
 - _exit (man 2 _exit)
 - fflush (man 3 fflush)
 - fork (man 2 fork)
 - free (man 3 free)
 - getcwd (man 3 getcwd)
 - getline (man 3 getline)
 - isatty (man 3 isatty)
 - kill (man 2 kill)
 - malloc (man 3 malloc)
 - open (man 2 open)
 - opendir (man 3 opendir)
 - perror (man 3 perror)
 - read (man 2 read)
 - readdir (man 3 readdir)
 - signal (man 2 signal)
 - stat (__xstat) (man 2 stat)
 - lstat (__lxstat) (man 2 lstat)
 - fstat (__fxstat) (man 2 fstat)
 - strtok (man 3 strtok)
 - wait (man 2 wait)
 - waitpid (man 2 waitpid)
 - wait3 (man 2 wait3)
 - wait4 (man 2 wait4)
 - write (man 2 write)
****
## Example of Use
* Compile the program to create the `hsh` executable file.
* run the executable as follows `./hsh`
* Enter basic commands like: `ls`, you can add flags along with `ls` command such as `-l`, `-la`
* press enter after entering the command
* to end the execution of the `simple_shell` program press `ctrl + d` or write the word `exit`
Shell could work like 2 tips.
Your shell should work like this in interactive mode:
## Example of Usage
````
ubunto@ubuntu:~/holbertonschool-simple_shell$ gcc -Wall -Wextra -Werror -pedantic *.c -o hsh
ubunto@ubuntu:~/holbertonschool-simple_shell$ ./hsh
echo Hello, This is an example
Hello, This is an example
ls
README.md  checkbuild.c  line_exec.c  shell.c  string.c
buildin.c  hsh		 linkpath.c   shell.h
^C
ls -l
total 64
-rw-r--r-- 1 root root   143 Aug 23 14:20 AUTHORS
-rw-r--r-- 1 root root  4148 Aug 23 19:27 README.md
-rw-r--r-- 1 root root   579 Aug 23 16:28 get_env.c
-rw-r--r-- 1 root root  1069 Aug 23 16:36 handle_path.c
-rwxr-xr-x 1 root root 17128 Aug 23 19:27 hsh
-rw-r--r-- 1 root root  1180 Aug 23 16:32 main.c
-rw-r--r-- 1 root root   395 Aug 23 16:35 main.h
-rwxr-xr-x 1 root root  2311 Aug 23 16:23 man_1_simple_shell
-rw-r--r-- 1 root root   225 Aug 23 16:32 print_env.c
-rw-r--r-- 1 root root   444 Aug 23 16:35 strcat.c
-rw-r--r-- 1 root root   484 Aug 23 16:22 trim.c
exit
ubunto@ubuntu:~/holbertonschool-simple_shell$
````
But also in non-interactive mode:
```
ubunto@ubuntu:~/holbertonschool-simple_shell$ echo "/bin/ls" | ./hsh
hsh main.c main.h test
ubunto@ubuntu:holbertonschool-simple_shell$ cat test
/bin/ls
/bin/ls
ubunto@ubuntu:~/holbertonschool-simple_shell$
ubunto@ubuntu:~/holbertonschool-simple_shell$ cat test | ./hsh
hsh main.c shell.c
hsh main.c shell.c
ubunto@ubuntu:~/holbertonschool-simple_shell$
```
## Error Handling
- If execve() cannot find or execute the specified command, the shell displays an error message, including a brief explanation of the error (using perror()), and then
  returns to the prompt.
- If the fork() call fails, the shell exits with an error message.
- Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.
- The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (See below)
### Description of what each file shows:
|Function|Description|
|----|-------|
|main.h|holds prototypes of functions spread across all files|
|main.c|holds main process code|
|handle_path.c|handling path from environment variables|
|print_env.c|printing environment variables with their values|
|strcat.c|concatting two different strings|
|trim.c|deleting white spaces from string|
|man_1_simple_shell|custom manpage for simple shell|
## Requirements

To compile and run the shell, you need:
> *C Compiler:* The source code is written in C, so you'll need a C compiler like GCC to compile it.

## Bugs
No known Bug.

## Authors
* Metin Abbaszade | [@Metin100](https://github.com/Metin100)
* Cavid Agayev | [@justjavid](https://github.com/justjavid)
