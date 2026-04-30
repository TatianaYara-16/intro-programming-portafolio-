

1. SECTION, Concept in my own words

I see nested loops as a "loop within a loop" situation. It's like having a master task and a sub-task that needs to be fully completed before the master
task can move to the next step. I imagine it like a grid or a calendar: the outer loop goes through the weeks, and for every single week, the inner loop
has to go through all seven days. It’s a bit more complex because you have to be very careful with the variables; if you use the same counter for both,
the whole thing breaks. It’s mostly used when you're dealing with rows and columns or any scenario where you need to repeat a repetition.

2. SECTION, Key C# Syntax 

EXAMPLE 

*/

for (int i = 1; i <= 5; i++) 
{
    Console.Write($"Row {i}: "); // Label for each row
    
    for (int j = 1; j <= 10; j++) // Inner loop: represents the columns
    {
        int result = i * j;
        Console.Write($"{result}\t"); 
    }
    
    Console.WriteLine(); 
}
/*

Outer Loop: Controls the "big picture" or how many rows we have.

Inner Loop: Completes its entire cycle for every single step the outer loop takes.

Grid Logic: The code inside the inner loop is where the actual work (like the multiplication) happens.

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

At first, my brain just couldn't track what was happening. I would look at the code and think that both loops were running at the same speed. It was
super confusing to understand why the inner loop had to "finish" before the outer loop could increment by one. I felt like I was getting lost in a
maze of curly braces.

b) What mistake were you making?

I made two big mistakes constantly. First, I would forget to put a Console.WriteLine() between the loops, so all my results would just print in one
giant, messy line that made no sense. Second, I would accidentally use i++ in both loops, which caused the outer loop to finish way too fast or
created weird logic errors that were a nightmare to debug in VS Code.

c) What finally made sense?

The logic finally clicked when we compared "hard-coding" a block of numbers versus using nested loops. At first, I thought writing five 
Console.WriteLine("12345") was easier, but then I realized that if the professor asked for a grid of 100x100, I would be stuck for hours. Seeing
how the outer loop manages the rows (like ln or i) and the inner loop handles the characters (like ch or j) taught me how to think in dimensions.
The most important thing I learned was the "flow": I understood that when you reach the end of the outer loop's body, you don't just stop; you 
must go back up to increment i++ and start the whole process again until the condition is met. It taught me that nested loops are all about 
efficiency and letting the computer handle the repetition that would be impossible for me to do manually.

4. SECTION, Describe one common mistake you made with this concept and why it happened. 

The "Semicolon Trap" is still a thing here, but the biggest issue is performance. If you make the loops too big (like 1000 x 1000), the computer 
has to do a million operations, and you can see the program slow down. Also, forgetting to use different variable names (like using i for both) 
is the number one reason why nested loops fail for beginners.

5.Research References

C# Programming Guide: Nested Control Structures and YouTube tutorials.
