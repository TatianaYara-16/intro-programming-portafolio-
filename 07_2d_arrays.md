/*
1. SECTION, Concept in my own words

I used to think of a normal array as a simple list or a single row of lockers. But a 2D Array is like an entire wall of lockers with rows and columns.
It’s basically a table. Instead of just one index, I now need two coordinates to find a value: the row number and the column number, like [row, col].
I learned that this is incredibly useful for things like building a game board, a seating chart, or even a simple mathematical grid. It’s like a
"nested variable"—a collection that grows in two directions at the same time.

2. SECTION, Key C# Syntax

To work with 2D arrays, we use a comma inside the brackets [,]. This tells C# we are dealing with dimensions (rows and columns).

EXAMPLE:

*/

Console.WriteLine("Enter rows and columns:");
int m = Convert.ToInt32(Console.ReadLine()); // rows
int n = Convert.ToInt32(Console.ReadLine()); // columns

int[,] grid = new int[m, n]; // Creating the table in memory

for (int i = 0; i < grid.GetLength(0); i++) 
{
    for (int j = 0; j < grid.GetLength(1); j++)
    {
        Console.Write($"Enter value for [{i},{j}]: ");
        grid[i, j] = Convert.ToInt32(Console.ReadLine());
    }
}

for (int i = 0; i < grid.GetLength(0); i++)
{
    for (int j = 0; j < grid.GetLength(1); j++)
    {
        Console.Write($"{grid[i, j]}\t");
    }
    Console.WriteLine(); // New line after each row is finished
}
/*

int[,]: The comma is the key; it defines the array as two-dimensional.

grid.GetLength(0): This gives me the number of rows.

grid.GetLength(1): This gives me the number of columns.

[i, j]: The coordinates. i is the row index, and j is the column index.

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

At first, I kept mixing up the rows and columns. I couldn't remember if the first number in grid[4, 5] was the horizontal or the vertical part. 
It was also confusing to use GetLength(0) and GetLength(1) instead of just .Length. I felt like I was back at the beginning, struggling to 
visualize how two loops were working together to fill a single "table."

b) What mistake were you making?

My biggest mistake was forgetting that grid.Length gives the total number of elements (like 20 if it's a 4x5), which totally breaks a for
loop meant for rows. I also struggled with the logic of cumulative sums—like in Exercise 12, where I forgot to reset or properly target the "total" 
row (the last row) when adding up the values from the other cells.

c) What finally made sense?

Everything clicked during Exercise 11 and 12. When I saw how I could use the j loop to move across a row and then the i loop to jump to the next line,
it finally looked like a real grid. The "Eureka" moment was realizing that I could use a 2D array to calculate totals automatically. For example, in 
the last exercise, we used the last row and last column to store the sum of the others (grid2[i, 3] += grid2[i, j]). Seeing the numbers align perfectly
in the console with the \t command made me realize that I wasn't just writing code; I was building a structured database in real-time based on what 
the user entered.

4. SECTION, Describe one common mistake you made with this concept and why it happened. 

The "Index Out of Range" is even more common here because you have two ways to fail! If you confuse GetLength(0) with GetLength(1), your loop will
try to access a column that doesn't exist in a row. Also, many beginners forget the Console.WriteLine() between the loops, which makes the 2D array
look like one long, confusing line of numbers instead of a nice table.

5. Research References
Microsoft C# Guide: Multidimensional Arrays and YouTube tutorials. */

