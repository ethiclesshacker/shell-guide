# Basic Command Line Utilities

## man
Before anything, `man` is the most important tool for any Linux user.

```sh
$ man man # Manual entry for the man tool
```
The usage and purpose of the `man` tool is very simple. It gives a user manual of sorts for the tool. Every system utility and most tools installed via package manager (such as apt) have a man page where you can find all the commands, optional flags, and sometimes even basic use case statements.

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
<details>
<summary> Advanced Uses</summary>

The ls tool has many optional flags that are useful for advanced users.

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
    $ ls -ls
    ```

</details>


## ps
## echo
## cat
## cal
## date
## uname
## exit