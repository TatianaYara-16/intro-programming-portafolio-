
/*
1. SECTION, Concept in my own words

I like to think of the foreach loop as a more "polite" and automated way to go through an array. Instead of me having to manage a counter like i and making sure
I don't go past the .Length, I just tell the computer: "For each item in this collection, do this." It’s much more natural, like saying "For each student in 
the class, give them a paper," instead of "Start with the first student, then move to the second, then the third, until you reach the end." It’s cleaner, easier
to read, and it practically eliminates those annoying "Off-by-one" errors because the loop handles the start and the end of the array automatically.

2. SECTION, Key C# Syntax 

The syntax is very straightforward. You define a temporary variable that represents the "current" item being processed.

EXAMPLE:
*/

float[] temperatureCollection = { -1.5f, 3.2f, 1.0f, 0.0f, 3.5f, -6.0f, 15.0f };

Console.WriteLine("Montreal Weekly Forecast:");

// Syntax: foreach (datatype variableName in arrayName)
foreach (float temp in temperatureCollection) 
{
    if (temp < 0) 
    {
        Console.WriteLine($"{temp}°C - Wear a winter coat!");
    }
    else 
    {
        Console.WriteLine($"{temp}°C - A light jacket is fine.");
    }
}
/*
Temporary Variable (float temp): This holds the value of the current element in each iteration.

The in Keyword: Links the temporary variable to the array you want to explore.

Read-Only Rule: One thing I learned is that you cannot change the values inside the array while using foreach; it’s only for reading or "iterating" through them.

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

At first, I didn't understand where the variable inside the foreach was coming from. I kept looking for where it was initialized (like int i = 0) and
I couldn't see it. It felt like "magic" that the program just knew when to stop without me telling it to check the .Length of the array.

b) What mistake were you making?

My biggest mistake was trying to use the foreach variable to change the data in the array. For example, I tried to do foreach (int grade in grades)
{ grade = grade + 5; } to give everyone extra points, and I was so frustrated when the compiler told me it was a "read-only" variable. I had to learn
that if I want to modify the array, I still need my old friend the for loop.

c) What finally made sense?

Everything clicked when I had to print out a long list of student grades. Using the for loop with grades[i] felt like I was doing extra work by 
constantly typing brackets and indices. When I switched to foreach (int grade in grades), the code looked so much cleaner and professional. 
I realized that foreach is for when you just want to "visit" every item to see what's inside or to do a calculation without changing the original list.
It made me appreciate how C# has different tools for different needs—for for when you need control, and foreach for when you just want simplicity.

4. SECTION, Describe one common mistake you made with this concept and why it happened.

The most common mistake is trying to modify the collection dding or removing items, while inside a foreach loop, which will crash your program.
Also, some people get confused and try to use an index like temp[i] inside a foreach, forgetting that the variable temp is already the value itself,
not a position.

5. Research References
Microsoft Learn: The foreach enumeration statement, Classroom activities and codes








