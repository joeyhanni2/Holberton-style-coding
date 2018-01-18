In order to keep your code maintainable and readable, you'll be asked to document every single function of all your source files.

### How to document functions

To document a function, you simply need to insert a comment block above it.
Instead of a regular C multiline comment, the comment block must begin with the following line:

```
/**
```

with two stars.  
Then, each line of the block must start with a star, followed by a space:

```
 * 
```

The block must end exactly like a C multiline comment, with a multiline comment closer:

```
 */
```

### Format of the documentation block

In the following description:

* `(...)?` signifies optional structure.
* `(...)*` signifies 0 or more structure elements

The format of a documentation block is the following one:

```C
/**
 * function_name - Short description, single line
 * @parameterx: Description of parameter x
(* a blank line
 * Description: Longer description of the function)?
(* section header: Section description)*
 * Return: Description of the returned value
 */
```

So the trivial example would be:

```C
/**
 * my_function - This is a description
 */
void my_function(void)
{
	do_something();
}
```

If the function must returns a value (anything but `void`), the `Return:` header tag is mandatory:

```C
/**
 * print_hello - Prints "Hello"
 */
void print_hello(void)
{
	printf("Hello");
}

/**
 * is_positive - Check if a number is greater than 0
 * @nb: The number to be checked
 *
 * Return: 1 if the number is positive. 0 otherwise
 */
int is_positive(int nb)
{
	return (nb > 0);
}
```

If there is one or more parameter described, then there must be a blank line after their specification (Only if there is something to describe after the parameters):

```C
/**
 * op_add - Makes the sum of two numbers
 * @arg1: First operand
 * @arg2: Second operand
 *
 * Return: The sum of the two parameters
 */
int op_add(int arg1, int arg2)
{
	return (arg1 + arg2);
}

/**
 * print_arg - Prints a string using printf
 * @arg: The string to be printed
 */
void print_arg(char *arg)
{
	print_string(arg);
}
```

Example for the `Description` header (longer description)

```C
/**
 * op_add - Makes the sum of two numbers
 * @arg1: First operand
 * @arg2: Second operand
 *
 * Description: This is a longer description.
 * Don't forget that a line should not exceed 80 characters.
 * But you're totally free to use several lines to properly
 * describe your function
 * Return: The sum of the two parameters
 */
int op_add(int arg1, int arg2)
{
	return (arg1 + arg2);
}
```

You can also add additional sections. For example, you can add a section `Example` on which you can give an example of usage when it's relevant.

Example:

```C
/**
 * op_add - Makes the sum of two numbers
 * @arg1: First operand
 * @arg2: Second operand
 *
 * Example:
 *    op_add(90, 8); --> 98
 */
int op_add(int arg1, int arg2)
{
	return (arg1 + arg2);
}
```