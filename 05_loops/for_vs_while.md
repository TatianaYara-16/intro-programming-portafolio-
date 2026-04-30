
1. SECTION, Concept in my own words

I’ve learned that for and while loops are like two different tools for the same job. A for loop is my go-to when I know exactly how many times I need to repeat
something before I even start—it’s very compact because the initialization, the condition, and the update all live on one line. On the other hand, a while loop 
is better when the number of repetitions is uncertain and depends on a condition that might change at any moment. The execution of a for loop feels very 
automated, while a while loop feels more like a continuous check
that keeps running as long as the "light is green."

2. SECTION, Key C# Syntax 

While both loops achieve repetition, their structure determines how we handle the control variable. In a for loop, everything is encapsulated, whereas in a 
while loop, the programmer is responsible for managing the state manually.

Use FOR when you have a specific range or a known number of items to process.

EXAMPLE FOR: */
int totalSum = 0;

for (int i = 1; i <= 10; i++) 
{
    totalSum += i; // Adding the current value of i to the total
    Console.WriteLine($"Iteration {i}: Current sum is {totalSum}");
}

Console.WriteLine("Final Result using For: " + totalSum);

// Use WHILE when the loop should continue until a specific condition changes, which might not happen at a fixed count.

//EXAMPLE WHILE 

int batteryLevel = 20;
int minutesPassed = 0;

while (batteryLevel > 0) 
{
    Console.WriteLine($"Minute {minutesPassed}: Battery at {batteryLevel}%");
    
    batteryLevel = 5; 
    minutesPassed++;
    
    if (batteryLevel == 5)
    {
        Console.WriteLine("Warning: Low battery!");
    }
}

Console.WriteLine("Phone shut down after " + minutesPassed + " minutes.");}

/*
3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

I used to think I had to pick one and stick with it for everything. It was confusing to see the same "Hello" result coming from two different structures.
I didn't understand why I would bother with the for syntax when while seemed more straightforward to read.  

b) What mistake were you making?

In while loops, I constantly forgot to add the count++ at the end, which caused my laptop to freeze in an infinite loop. In for loops, I often got
"Off-by-one" errors, where my loop would run 4 times instead of 5 because I was confused between using < or <= in the condition.

c) What finally made sense?

It clicked when we did the exercise of saying "Hello" 5 times using both methods. I realized that the for loop is much "cleaner" because it forces you
to put the update (i++) right at the top, so you can't forget it. I learned that for is for counting and while is for waiting for something to happen.

4. SECTION, Describe one common mistake you made with this concept and why it happened. 

The most common mistake is definitely the infinite loop in the while structure because the update step is physically separated from the condition. 
Also, many beginners (including me) accidentally put a semicolon after the for statement for(...);, which makes the loop do absolutely nothing and then
run the code block only once.

5.Research References

I used the material from our class activities and YouTube tutorials and Microsoft Learn: Iteration statements (for, foreach, while, and do).

