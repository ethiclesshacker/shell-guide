# Basic Command Line Utilities

## man
Before anything, `man` is the most important tool for any Linux user.

```sh
$ man man # Manual entry for the man tool
```
The usage and purpose of the `man` tool is very simple. It gives a user manual of sorts for the tool. Every system utility and most tools installed via package manager (such as apt) have a man page where you can find all the commands, optional flags, and sometimes even basic use case statements.

## whatis
The what is command lists the first line, usually the name, from the `man` page of it's parameter.

```sh
$ whatis bash
bash (1)      - GNU Bourne-Again SHell
```

## pwd
The directory the terminal is in, or the program is being run from is known as the **p**resent **w**orking **d**irectory. `pwd` returns the full path to the present working directory.
```sh
$ pwd
/home/aadityavs
```

## cd
Probably the most used tool in day-to-day applications. `cd` is the Change Directory tool. It is used to change directory using absolute or relative file paths.
```sh
$ pwd
/home/aadityavs
$ cd /
$ pwd
/
$ cd ~
$ pwd
/home/aadityavs/
```

## ls
The `ls` tool lists all files, folders, and even hidden ones with certain flags.
```sh
$ ls
Assignments Downloads Music Projects Shell Templates
```

The `ls` tool also prints in a long list format with a lot of other data related to each file/directory in the present working directory, using the `-l` flag.

```sh
$ ls -l
# Give output here.
```


<details>
<summary> Advanced Uses </summary>

The `ls` tool has many optional flags that are useful for advanced users.

- List hidden files and folders.
    ```sh
    $ ls -a
    ```
- List hidden files and folders, without current and parent directory
    ```sh
    $ ls -A
    ```
- List directories first
    ```sh
    $ ls -g
    ```
- List sizes in human readable format while using the `-l` flag
    ```sh
    $ ls -lh
    ```
- List everything sorted with timestamps while using the `-l` flag
    ```sh
    $ ls -lt
    ```
- List everything sorted according to filesize while using the `-l` flag
    ```sh
    $ ls -lS
    ```

</details>


## echo
Honestly, this is the one command in almost every shell script, used for printing to the standard output (which can be redirected to a file if needed.)

```sh
$ echo "Hello World!"
Hello World!
```
Using the `-n` flag will prevent `echo` from adding a new line after the given string.

```sh
$ echo -n "Hello World!"
Hello World!$
```
> The dollar symbol $ is the prompt of the terminal, just after the output of the echo command.

By default, the `echo` command does not interpret escape sequences like C or other languages do. This can be enabled with the `-e` flag.

```sh
$ echo -e "Hello\nWorld!"
Hello
World!
```

## cat
The cat command reads a file and prints the contents of the file to standard output.

```sh
$ cat data.txt
Hello World!
```

While there are many flags, the most useful ones are as follows.

The `-n` flag is used to number all the output lines.
```sh
$ cat -n data.txt
1 Hello World!
2
3 Third line
```

The `-b` flag is used to number only the non blank lines.
```sh
$ cat -n data.txt
1 Hello World!

2 Third line
```

The `-E` flag is used to show a **$** dollar sign at the end of every line printed to the standard output.
```sh
$ cat -n data.txt
Hello World!$
$
Third line$
```


## cal
This is a program which is less and less used, and more carried over from the days Unix/Linux systems didn't have a graphical user interface. While it has a lot of options one can deal with, only two common/possible options will be shown.
```sh
$ cal               # Default operation
    August 2020       
Su Mo Tu We Th Fr Sa  
                   1  
 2  3  4  5  6  7  8  
 9 10 11 12 13 14 15  
16 17 18 19 20 21 22  
23 24 25 26 27 28 29  
30 31 
```

Also, we can see the calendar for previous, current and next month, using the `-3` flag.

```sh
$ cal -3
                            2020
        July                 August              September        
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
          1  2  3  4                     1         1  2  3  4  5  
 5  6  7  8  9 10 11   2  3  4  5  6  7  8   6  7  8  9 10 11 12  
12 13 14 15 16 17 18   9 10 11 12 13 14 15  13 14 15 16 17 18 19  
19 20 21 22 23 24 25  16 17 18 19 20 21 22  20 21 22 23 24 25 26  
26 27 28 29 30 31     23 24 25 26 27 28 29  27 28 29 30           
                      30 31
```

## date
While it is similar to the `cal` command in the sense that it is also brought over from the days when systems lacked a GUI, the `date` command still finds it's use in some scripting purposes, and in the internal logging of certain tools.

```sh
$ date
Friday 28 August 2020 08:31:19 PM IST
```

We should also learn how to print the date or time in a custom format.

```sh
$ date +%m-%d-%Y
08-28-2020
$ date +%H:%M:%S
20:37:53
```

## exit

The `exit` command is simple. If written in the terminal directly, it closes the terminal session; and if written in a shell script, it terminates the execution of the script.


More on Shell Scripting in a later module.