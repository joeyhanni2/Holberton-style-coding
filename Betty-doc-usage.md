To check your C source files or C header files documentation, you can run `betty-doc` script as follows:

```ShellSession
./betty-doc.pl file
```

Examples:

```ShellSession
./betty-doc.pl main.c
```

```ShellSession
./betty-doc.pl main.c crack_passwd.c utils.h
```

```ShellSession
./betty-doc.pl src/*.c include/*.h
```

You can see all available options for `betty-doc` by running the script as follows:

```ShellSession
./betty-doc.pl -h
```