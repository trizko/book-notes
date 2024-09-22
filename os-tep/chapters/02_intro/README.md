# Chapter 02 - Introduction to Operating Systems

# Notes (Reading)

- The point of an OS is to create an environment that makes it easy to write programs against.
    - This is accomplished through creating interfaces for virtualization, concurrency, and persistence.
    - Those 3 concepts will be the cornerstone of the entire rest of the book.

# Notes (Code)
The code samples come with header files that are not natively on your operating system. They must be retrieved from either the tarball bundle or from the github repository found here: https://github.com/remzi-arpacidusseau/ostep-code/tree/master/intro

To compile and run the code, use the following command:
```bash
gcc -o name_of_binary program_filename.c -Wall
./name_of_binary
```

There are examples where the authors run the code as multiple processes at the same time with the `&` symbol. This assign a process identifier (PID) to each running program and run them in the "background". To exit all of these you, you must either, one by one, put the process in the foreground with the `fg` command and then ctrl-c out for each process or you can open another terminal window and use the `kill` command with a list of each PID you would like to terminate, like so:
```bash
kill 11111 11112 11113
```
The above command will send the signal `TERM` (terminate - this is what ctrl-c does when a process is in the foreground) to the processes `11111`, `11112`, and `11113`. You can specify which signal to send with the `-s` command but the `TERM` signal is usually the default.