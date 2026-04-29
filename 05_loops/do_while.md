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



