*/1. SECTION, Concept in my own words

I think of a do-while loop as the "shoot first, ask questions later" version of a loop. Unlike other loops that check the condition at the beginning,
the do-while always runs the code inside at least once before checking if it should repeat. It’s like a trial period for an app; you get to try it once,
and then the program checks if you have a valid subscription to keep using it. The execution flows straight into the do block, runs the instructions, 
and only then hits the while condition at the bottom. If the condition is true, it jumps back up to the do; if not, it exits.

2. SECTION, Key C# Syntax 

The do-while loop is unique because it ends with a semicolon after the condition.

EXAMPLE: */

do 
{
    Console.Write("Enter a grade between 0 and 100: "); // The program asks for the grade at least once
    studentGrade = Convert.ToInt32(Console.ReadLine());

    if (studentGrade < 0 || studentGrade > 100)
    {
        Console.WriteLine("Invalid entry. Please try again.");
    }

} while (studentGrade < 0 || studentGrade > 100); 
// The loop repeats IF the grade is outside the valid range

Console.WriteLine("Grade accepted: " + studentGrade);

*/

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

I didn't understand why I would ever need a loop that runs before checking the condition. It felt safer to always check first (like in a while loop) to avoid errors. I also kept forgetting the semicolon at the end of the while line, which made me feel like I didn't understand the syntax at all.


b) What mistake were you making?

My biggest mistake was using it for things that shouldn't run if the initial data was wrong. For example, in a lab where we had to process numbers, I used a do-while, and it processed a "0" that I didn't want because the check happened too late. I also struggled with infinite loops because I would forget to increment my counter inside the do block.

c) What finally made sense?

I learned the real difference between loops when we practiced "Repeating the Play" versus "Fixed Counting". I finally understood that a do-while is the most logical tool when you don't know the exact number of entries beforehand, as it allows the user to decide when to stop via a "control question" like (y/n). It clicked that this loop treats the first interaction as a guarantee and the rest as an option, which is much more efficient for real-world tasks like entering student grades one by one. Experimenting with both incrementing (count++) and decrementing (count--) also showed me I could manage the same data from different directions as long as my exit condition was solid.

4. SECTION, Describe one common mistake you made with this concept and why it happened. 

The most frustrating mistake is definitely the infinite loop. If you forget to update the variable used in the condition (like counter++), the condition stays true forever, and Visual Studio Code just hangs or the console fills up with text until the program crashes. Also, forgetting the semicolon at the very end of the statement is a classic syntax error.

5. Research References
Microsoft C# Documentation: do-while statement and YouTube tutorials.*/



