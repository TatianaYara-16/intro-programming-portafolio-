
/*
1. SECTION, Concept in my own words

I used to think of variables like single folders on a desk, but after studying Arrays, I see them as a big filing cabinet where everything is organized and labeled
with a number. An Array is a collection of data of the same type that lives under a single name. Instead of creating thirty different variables for thirty students,
I create one Array and access each student using an "index." The most important thing to remember is that in C#, we start counting at zero, not one. So, the first
person in the line is at position 0. It makes my code so much cleaner because I can use a single loop to process hundreds of pieces of information at once, like 
temperatures for a whole year or grades for a full classroom.

2. SECTION, Key C# Syntax

The way we create arrays can vary depending on whether we already know the data or if we need to ask for it later. Here are the different ways I've learned
to set them up:

EXAMPLE
*/ 

float[] weeklyTemp = { -1.5f, 3.0f, 1.2f, 0.5f, 3.2f, -6.0f, 15.0f };

float[] amTemp = new float[365]; // This creates 365 empty slots for floats

Console.WriteLine("How many students are in the class?");
int size = Convert.ToInt32(Console.ReadLine()); 

int[] studentGrades = new int[size]; 

for(int i = 0; i < studentGrades.Length; i++)
{
    Console.WriteLine($"Please enter the grade for student {i + 1}:"); 
    studentGrades[i] = Convert.ToInt32(Console.ReadLine());
}

Console.WriteLine("\n--- Class Results ---");
for (int i = 0; i < studentGrades.Length; i++)
{
    Console.WriteLine($"Student {i + 1} (Index {i}): {studentGrades[i]}"); 
}
/*

datatype[]: The brackets tell C# this isn't just one value, but a collection.

Length: A super useful property that tells me exactly how many slots are in the array.

new: The keyword used to "instantiate" or build the array object in the computer's memory.

Index ([i]): The address of a specific value inside the array.


3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

The "Zero-Based Indexing" was a total headache for me. I couldn't understand why the 10th student in my class was sitting at grades[9] instead of grades[10].
It felt very unnatural. Also, the difference between declaring an array (int[] grades) and actually building it with new int[size] was confusing; I thought
just giving it a name was enough to start using it.

b) What mistake were you making?

I kept getting the "IndexOutOfRangeException" error because I would try to run my loops one step too far. For example, if my array had a length of 5,
I would try to access grades[5], forgetting that the last valid index is actually 4. Another mistake was trying to print the whole array by just saying
Console.WriteLine(grades), which just showed me the type name instead of the actual numbers I stored.

c) What finally made sense?

Everything clicked when we did the exercise comparing individual variables (grade1, grade2...) vs. an Array. I realized that if the professor had 730
temperature readings to record, creating 730 separate variables would be impossible. Seeing how I could use Convert.ToInt32(Console.ReadLine()) 
to let the user decide the size of the array "live" during interaction was a game-changer. I understood that an array isn't just a list; it's a
dynamic structure that allows my program to grow or shrink based on what the user needs, and using a for loop with grades.Length is the only way
to handle all that data without making a mess.

4. SECTION, Describe one common mistake you made with this concept and why it happened.

The biggest one is definitely the "Off-by-one" error, where you either start at index 1 (missing the first element) or try to reach an index equal
to the .Length (crashing the program). Also, many people forget that once you set the size of an array in C#, you can't change it; if you need more space,
you have to create a brand new, bigger array.

5.Research References

Microsoft C# Documentation: Arrays (C# Programming Guide) and slassroom exercises on dynamic array.













