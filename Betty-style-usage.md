To check your C source files or C header files coding style, you can run `betty-style` script as follows:

```ShellSession
./betty-style.pl file1 [file 2 [file3 [...]]]
```

Examples:

```ShellSession
./betty-style.pl main.c
```

```ShellSession
./betty-style.pl main.c crack_passwd.c utils.h
```

```ShellSession
./betty-style.pl src/*.c include/*.h
```

You can see all available options for `betty-style` by running the script as follows:

```ShellSession
./betty-style.pl --help
```