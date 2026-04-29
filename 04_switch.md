Console.WriteLine("Hello, World!");
/*
1. SECTION, Concept in my own words

I look at the switch statement as a more organized way to handle multiple choices. Instead of using
a long chain of if-else blocks that can get messy, a switch takes a single variable and compares 
its value against different "cases." It’s like an elevator: you press a button for a specific floor
(the case), and the elevator takes you directly there. Each case has a break at the end to tell 
the program to stop and exit the switch once the job is done. It’s very useful for things like menu
selections or days of the week because it makes the code much cleaner and easier to read for other 
programmers.

2. SECTION, Key C# Syntax 

The switch uses a selector (the variable) and matches it to a case label.

example:*/

int dayNumber = 3;

switch (dayNumber) // dayNumber is the selector
{
    case 1:
        Console.WriteLine("Monday");
        break; // break is mandatory to exit the block
    case 2:
        Console.WriteLine("Tuesday");
        break;
    default: // default runs if no cases match
        Console.WriteLine("Another day");
        break;
}

/*
3. SECTION, Eureka Exercise/Moment

a) What was confusing at first? 

I didn't understand why I needed a switch if I already knew how to use if-else. It felt redundant.
Also, the default keyword was confusing because I wasn't sure if it was mandatory or what its real
purpose was in a simple program.

b) What mistake were you making? 

My biggest mistake was forgetting the break keyword at the end of each case. In C#, if you forget 
the break, the program throws an error because it doesn't know where to stop. I also tried to use
comparison operators like case > 10:, which I later learned doesn't work that way in a basic switch
statement.

c) What finally made sense? 

Everything clicked for me during the Exercise in class, where we had to determine the day of the week
based on a date calculation. At first, I wrote a long chain of if-else statements to check if d0 
was 0, 1, 2,and so on. It worked, but it looked like a giant wall of repetitive code. When we implemented
the same logic using a switch statement, I finally saw the power of "grouping" cases. For example, being
able to group cases 1 through 5 to simply print "Week Day" or cases 0 and 6 for "WeekEnd!" showed 
me that a switch isn't just a different way to write an if; it's actually much more efficient for
categorizing data. It also taught me to always check the documentation, because I initially thought
Sunday was 7, but the formula taught me it was 0.


4. SECTION, Describe one common mistake you made with this concept and why it happened. 

As I mentioned before, forgetting the break; is the most common error. Another one is trying to use
a switch with data types that don't match well, or repeating the same value in two different cases,
which causes a compiler error in Visual Studio.

5.Research References

I used the material from our class activities, Microsoft C# Guide: The switch statement, chat gpt for
understand the diference between if else and switch and YouTube tutorials.*/


