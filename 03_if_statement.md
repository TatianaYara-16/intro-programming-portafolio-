
1. SECTION, Concept in my own words


I think of an if statement as a fork in the road for my code. It’s a tool that allows the program to check if a specific condition is true before running
a block of code. If the condition is met, the program enters the "gate" and executes the instructions inside; if not, it simply skips everything and moves
to the next part of the script. This is super important because it’s how we make programs interactive, like checking if a user entered the right password
or if a player has enough points to level up. The execution flows straight down, but the if statement decides if a certain "branch" of code gets to run or not.

2. SECTION, Key C# Syntax

To write an if statement, we use the if keyword followed by a condition inside parentheses. If we need an alternative for when the condition is false, we use an else block.

Example:

int currentTemp = -10; // It's cold in Montreal!

if (currentTemp < 0) // The 'condition' is inside the parentheses
{
    Console.WriteLine("Wear a heavy coat!");  // This is the 'loop body' or code block that runs if true
}
else 
{  
    Console.WriteLine("A light jacket is fine."); // This runs if the condition is false
}

Condition: A boolean expression (something that results in true or false).

Code Block: The area inside the curly braces { } that contains the instructions.

Else: An optional part that handles what happens when the if condition is not met.

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first? 

At the beginning, I struggled to understand how the computer decided which path to take when there
were multiple conditions. I used to think the program would check every single block of code regardless 
of the result, and I couldn't wrap my head around how a "True" or "False" result could actually make 
the execution skip entire sections of my script.

b) What mistake were you making?

I kept trying to write conditions as if I were speaking English, like writing if (grade is 60 or more). Also, I frequently forgot that the else block doesn't need
its own condition in parentheses; I would try to write else (condition) and get a syntax error in Visual Studio every single time.

c) What finally made sense? 

The moment this finally made sense to me was during the "Grade Calculator" midterm exam. I was struggling to understand how to tell the program that a score of 60 was
a "Pass" but 59 was a "Fail." When I saw how the if statement acts like a filter, it clicked. I realized I could just write if (grade >= 60) and the computer 
would automatically handle thousands of different numbers for me without me having to check each one manually.

4. SECTION, Describe one common mistake you made with this concept and why it happened.

A very common mistake I made was putting a semicolon ; right after the condition, like if (age > 18);. This is a nightmare to debug because C# thinks the if
statement is finished right there, so it runs the code below it no matter what. It took me a few labs to realize that the curly braces are what should follow 
the condition, not a semicolon.

5.Research References

Microsoft Learn: C# Conditional Statements.




