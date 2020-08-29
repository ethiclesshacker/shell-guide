# System Utilities

## ps
The `ps` command, is the utility for Process Selection. While it is not exactly used to operate on any of those processes, it's still a good tool to know because it helps to get the process id for operating on a process. 
> Such operations, however, are beyond the scope of this guide.

The most common flag for the ps command is `-e`. 
```sh
$ ps -e
# List of all current processes here
```
<!-- Add one more command here. -->
```sh
$ ps 
```



## uname
This is a tool which gives a lot of details about the current system, and has a lot of flags related to getting those values. While we will see only a few of the flags, see the `man` page of `uname` to find a list of all flags and their corresponding values.

```sh
$ uname         # kernel name
Linux
```

```sh
$ uname -n      # hostname
avs
```

```sh
$ uname -v      # kernel version
46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020
```

```sh
$ uname -a      # All details
Linux avs 5.4.0-42-generic "#"46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux
```