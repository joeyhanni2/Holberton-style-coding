Functions should be short and sweet, and do just one thing.  
They must fit on **40 lines**, and do one thing and do that well.

The maximum length of a function is inversely proportional to the complexity and indentation level of that function.  
So, if you have a conceptually simple function that is just one long (but simple) case-statement, where you have to do lots of small things for a lot of different cases, it's OK to have a longer function.

However, if you have a complex function, and you suspect that a less-than-gifted first-year high-school student might not even understand what the function is all about, you should adhere to the maximum limits all the more closely.  
Use helper functions with descriptive names (you can ask the compiler to in-line them if you think it's performance-critical, and it will probably do a better job of it than you would have done).

Another measure of the function is the number of local variables.  
They shouldn't exceed `5-10`, or you're doing something wrong.  
Re-think the function, and split it into smaller pieces.  
A human brain can generally easily keep track of about 7 different things, anything more and it gets confused.  
You know you're brilliant, but maybe you'd like to understand what you did 2 weeks from now.

In source files, separate functions with one blank line.