The other issue that always comes up in C styling is the placement of braces.  
Unlike the indent size, there are few technical reasons to choose one placement strategy over the other, but the preferred way, is to put both the opening and the closing braces first, thusly:

```C
	if (x == 1)
	{
		some_code = here;
	}
```

This applies to almost all non-function statement blocks: `if, switch, for, while`.  
**E.g.:**

```C
	switch (action)
	{
	case CASE_ADD:
		return ("add");
	case CASE_REMOVE:
		return ("remove");
	case CASE_CHANGE:
		return ("change");
	default:
		return (NULL);
	}
```

and

```C
	if (x == y)
	{
		...
	}
	else if (x > y)
	{
		...
	}
	else
	{
		....
	}
```

This applies to functions too: they have the opening brace at the beginning of the next line, thus:

```C
	int function(int x)
	{
		body of function
	}
```

### Exceptions

Note that the closing brace is empty on a line of its own, **except** in the cases where it is followed by a continuation of the same statement, ie a `while` in a `do-statement`, like this:

```C
	do {
		body of do-loop
	} while (condition);
```

Do not unnecessarily use braces where a single statement will do.

```C
	if (condition)
		action();
```

and

```C
	if (condition)
		do_this();
	else
		do_that();
```

This does not apply if only one branch of a conditional statement is a single statement; in the latter case use braces in both branches:

```C
	if (condition)
	{
		do_this();
		do_that();
	}
	else
	{
		otherwise();
	}
```