### Function prototypes

All your function prototypes must be declared in header files.

```C
/* this prototype has to be declared in a header file */
void sample_func(int);
```

### Structs, Enum, Unions definitions

All your structs, enums and union must be defined in header files.

```C
struct sample_struct
{
	int val;
	char *str;
};
```

```C
enum sample_enum
{
	FIRST = 1,
	SECOND,
	THIRD
};
```

and

```C
union color
{
	unsigned int ui32_value;
	unsigned char[4] rgba;
};
```

### Typedefs

All your typedefs must be defined in header files.

```C
typedef unsigned char uchar;

typedef struct sample_struct
{
	int value;
	char *str;
} sample_struct;
```

### Double inclusion

To prevent double inclusion, we expect you to protect your header files by defining a macro, only if the header file hasn't been included yet.  

Example for a file named `sample_header.h`:

```C
#ifndef _SAMPLE_HEADER_H_
#define _SAMPLE_HEADER_H_

/*
 * Structs, enums and unions definitions
 * Typedefs
 * Function prototypes
 */

#endif /* _SAMPLE_HEADER_H_ */
```