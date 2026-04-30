
/*
1. SECTION, Concept in my own words

I think of Functions as "skill sets" that I give to my program. Instead of having one giant, messy block of code that does everything, 
I break it down into small, specialized "recipes." For example, if I need to calculate a sum or greet a user, I create a specific function
for that task. This makes my code much more organized because I only write the logic once (the definition) and then I can "call" it whenever
I need it. It’s like having a team of experts: one knows how to add numbers, another knows how to say hello, and I just call the one I need
at the right moment.

2. SECTION, Key C# Syntax

The structure of a function is very specific because the computer needs to know what it requires, what it does, and what it gives back.

A function definition always follows this pattern: returnType FunctionName(parameters) { body }.

Return Type: This is the "output" of the function. If it gives me back a number, I use int or double. If it just performs an action
(like printing to the console) and gives me nothing back, I use the keyword void.

FunctionName (PascalCase): we always use PascalCase (starting every word with a Capital letter)
and choose informative names that describe exactly what the function does, like AddTwoNumbers.

Formal Parameters: These are the "ingredients" the function needs from the outside to operate. They live inside the parentheses ().
If the function doesn't need external data, the parentheses stay empty.

The Body: Everything inside the curly braces {} is the actual work being done.

EXAMPLE:
*/
void SayHello1(string aName) 
{
    Console.WriteLine("Operating from SayHello1");
    Console.WriteLine($"Hello, {aName}!");
}

// Example 2: 
int AddTwoNumbers(int num1, int num2) 
{
    int sum = num1 + num2;
    return sum; // The "return" keyword sends the result back to the caller
}

SayHello1("Jessica"); 
int result = AddTwoNumbers(10, 5); 

/*
3. SECTION, Eureka Exercise/Moment

a) What was confusing at first?

The difference between a Parameter and an Argument was very confusing. I didn't understand that a parameter is the "placeholder" inside the function definition,
while the argument is the "real value" I send when I call it. Also, the return keyword felt weird; I thought that if the function printed something to the screen,
that was the "return," but I learned they are two completely different things.

b) What mistake were you making?

I used to forget that if I define a function with a return type like int, I must use the return keyword at the end, or the code won't compile. I also struggled 
with the scope of variables; I would try to use a variable created inside AddTwoNumbers out in my Main code, and I didn't understand why the computer couldn't "see" it.

c) What finally made sense?

It finally clicked when we practiced the different ways to greet a user. I saw that with SayHello(), the function was "closed" because it asked for the name inside 
its own body, but with SayHello1(name), it was much more flexible because I could get the name from anywhere in my program and then just "send" it to the function.
Comparing AddTwoNumbers (which uses a temporary variable for the sum) versus SumTwoNumbers (which just returns the math directly) showed me that I can write functions
in different ways as long as the logic is clear. It made me realize that functions are the secret to building professional software that isn't just one long, confusing
script.

4. SECTION, Describe one common mistake you made with this concept and why it happened. 

A classic mistake is forgetting the () when calling a function that has no parameters, like writing SayHello; instead of SayHello();. Also, many beginners try to define
a function inside another function, which is not allowed in basic C# structure. You have to define them separately and then call them.

5.Research References

Microsoft Learn: Methods (C# Programming Guide), W3Schools: C# Methods and Parameters and classroom activities.




