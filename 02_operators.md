*/ 1 SECTION. Concept in my own words

I see operators as the "tools" we use to manipulate the data stored in our variables. They are like the verbs of a sentence; they tell the computer what to do with the
numbersor strings we give it. For example, we use arithmetic operators for basic math, but we also use comparison operators to ask questions, like "is this number bigger
than that one?". The execution is simple: the program takes the values (operands), applies the operator's logic, and usually produces a new result or a true/false answer.
Without them, our variables would just sit there in memory without actually doing anything useful for our app.

2. SECTION, Key C# Syntax 

In C#, we have different categories of operators. The most common ones are for math and for comparing values to make decisions later in the code.

 example arithmetic operators
 
int totalDogs = 5 + 2;        // Addition (+)
int change = 20 - 15;         // Subtraction (-)
int remainder = 10 % 3;       // Modulo (%) -

 example Comparison Operators (result is always a bool)

 
bool isCold = temp < 0;       // Less than (<)
bool isEqual = (5 == 5);      // Equality (==) 

3. SECTION, Eureka Exercise/Moment

a) What was confusing at first? 

This concept finally clicked for me during the "Modulo" lab. At first, I didn't understand why I would ever need the remainder of a division. But when we had to
write a program to check if a number was even or odd, I realized that number % 2 == 0 was the perfect solution. It was like a lightbulb went off because I saw a
real use for math that seemed "extra" before.

b) What mistake were you making? 

A mistake I made a lot at the start was using a single equals sign = when I actually wanted to compare two things. I forgot that = is for assignment (putting a
value in a box) and == is for comparison (asking if they are the same). My code would often give me errors or change my variables by accident because of this, 
Besides that, I also made many mistakes in the correct use of and (&&) and or (||).

c) What finally made sense? 

Regarding the use of (=) and (==), I think it was a matter of paying attention and remembering the difference between the two and their proper use. However, and and
or became easier for me to understand when the professor explained it using a cup and a small ball—the ball could only be in one cup at a time, not in two at once,
which is similar to what happens when using and, since something cannot be in two places at the same time.

4. SECTION, Describe one common mistake you made with this concept and why it happened.

One mistake I made a lot was using a single equals sign = when I actually wanted to compare two things. In C#, = is for assignment (putting a value in a box), but ==
is for comparison (checking if they are the same). It’s frustrating because the code sometimes runs but gives the wrong result, or VS Code gives an error that is
hard to understand at first, Also, when I used or (||) instead of and (&&), or vice versa.

5.Research References

I used the material from our class activities, C# Documentation on Operators (Microsoft Learn), i Consulted Chat GPT to help to understand the diference between 
each operators and its use.















