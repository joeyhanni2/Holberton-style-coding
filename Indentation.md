### Purpose

> The whole idea behind indentation is to clearly define where a block of control starts and ends.  
> Especially when you've been looking at your screen for 20 straight hours, you'll find it a lot easier to see how the indentation works if you have large indentations.

___

### Tabs

Use `tabs` to indent your code.
Tabs characters will be counted as `1` character by `Betty`.

The preferred way to ease multiple indentation levels in a switch statement is to align the `switch` and its subordinate `case` labels in the same column instead of `double-indenting` the `case` labels.  
**E.g.:**

```C
int sample_func(char suffix)
{
	int var;

	var = 0;
	switch (suffix)
	{
	case 'G':
	case 'g':
		var = 30;
		break;
	case 'M':
	case 'm':
		var = 20;
		break;
	case 'K':
	case 'k':
		var = 10;
	default:
		break;
	}
	return (var);
}
```
___
Don't put multiple statements on a single line:

```C
	if (condition) do_this;
	do_something_everytime;
```

Don't put multiple assignments on a single line either.  
Betty coding style is super simple.  
___
Outside of comments and documentation, spaces are never used for indentation, and **the above example is deliberately broken.**

Get a decent editor and don't leave whitespace at the end of lines.