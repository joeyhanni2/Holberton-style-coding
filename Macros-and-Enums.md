Names of `macros` defining constants and labels in `enums` are capitalized.

```C
#define CONSTANT 0x12345
```

and

```C
enum sample
{
	FIRST = 1,
	SECOND,
	THIRD
};
```

Enums are preferred when defining several related constants.

CAPITALIZED macro names are appreciated but macros resembling functions may be named in lower case.

Generally, `inline functions` are preferable to macros resembling functions.

Macros with multiple statements should be enclosed in a `do - while` block:

```C
#define macrofun(a, b, c) \
	do \
	{ \
		if (a == 5) \
			do_this(b, c); \
	} while (condition)
```

___

### Things to avoid when using macros:

#### 1) Macros that affect control flow:

```C
#define FOO(x) \
	do \
	{ \
		if (bar(x) < 0) \
			return (-1); \
	} while (condition)
```

This is a _very_ bad idea.  
It looks like a function call but exits the `calling` function; don't break the internal parsers of those who will read the code.

#### 2) Macros that depend on having a local variable with a magic name:

```C
#define FOO(val) bar(index, val)
```

might look like a good thing, but it's confusing as hell when one reads the code and it's prone to breakage from seemingly innocent changes.

#### 3) Forgetting about precedence: macros defining constants using expressions must enclose the expression in parentheses. Beware of similar issues with macros using parameters.

```C
#define CONSTANT 0x4000
#define CONSTEXP (CONSTANT | 3)
```

#### 4) Namespace collisions when defining local variables in macros resembling functions:

```C
#define FOO(x) \
({ \
	typeof(x) ret; \
	ret = calc_ret(x); \
	(ret); \
})
```

`ret` is a common name for a local variable. `__foo_ret` is less likely to collide with an existing variable.