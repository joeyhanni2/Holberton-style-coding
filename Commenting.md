Comments are good, but there is also a danger of over-commenting.  
**NEVER** try to explain HOW your code works in a comment: it's much better to write the code so that the _working_ is obvious, and it's a waste of time to explain badly written code.

Generally, you want your comments to tell WHAT your code does, not HOW.
Also, try to avoid putting comments inside a function body: if the function is so complex that you need to separately comment parts of it, you should probably go back to chapter 6 for a while.  
You can make small comments to note or warn about something particularly clever (or ugly), but try to avoid excess.  
Instead, put the comments at the head of the function, telling people what it does, and possibly WHY it does it.

When commenting your functions, please use the betty-doc format.
See the Chapter about Documentation and the script `betty-doc` from Betty for details.

Betty style for comments is the **C89 style**.

```C
/* Use this */
```

**Don't use C99-style comments**

```C
// Don't use this
```

The preferred style for long (multi-line) comments is:

```C
	/**
	 * This is the preferred style for multi-line
	 * comments in C source code.
	 * Please use it consistently.
	 *
	 * Description:  A column of asterisks on the left side,
	 * with beginning and ending almost-blank lines.
	 */
```