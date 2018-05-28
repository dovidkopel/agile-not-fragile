## Computer Basics

What is a computer? The Oxford dictionary defines a computer as *An electronic device for storing and processing data, typically in binary form, according to instructions given to it in a variable program.* 
What I take from that is that computers store and process data, taking input from a software program.

>A computer would deserve to be called intelligent if it could deceive a human into believing that it was human. -Alan Turing

It is important to understand how a computer functions at the most primitive level.

The beginning of software engineering is understanding logic. The key to a successful engineer is being a problem solver and having a formidable toolbox. You need to learn what questions to ask, when to say I don't know and when you don't want to know. Essentially, a software engineer knows enough about the situation at hand to ask the pertinent questions. 

## Critical Thinking
Let's jump right into some logic problems and attempt to solve them. We will ask a question and then come up with a solution. Finally, we will represent the logic in pseudo code. That is not real code that can be executed on a computer, but it accurately describes the logical steps that code would possess.

#### If you take the name *John* and the name *Tim*, what do I need to do to know if they are the same length?

You start by evaluating that John is 4 characters, and Tim is 3. Then you take the values 4 and 3 and compare them for equality. Of course we know just by looking that the two names that they are in fact not equal in length, but behind the scenes that is a necessary calculation we make. For very long words we would need to actually calculate how many characters by counting them up...that is what computers excel in. Simple repetitive computation. Taking a word and moving character to character adding a value to the count until you have reached the end of that words. For a value that may have hundreds or thousands of characters that would take a person a long time...but a computer a mere fraction of a second.

Now let's see pseudo code that represents that logic.
```
# Initialize a variable for the name John
initial-name = "John"
# Initialize a variable for the name Tim
compare-name = "Tim"
# Check if the two have equivalent lengths
if length(initial-name) == length (compare-name)
    # Output a message indicating they are the same length
    print "the names are the same length."
# If the two are not equivalent     
else 
    # Output a message indicating they are not the same length
    print "the names are not the same length." 
```

#### Prove that the phrase "A man, a plan, a canal: Panama." is a palindrome.  
*A palindrome is a word, phrase or sequence that reads the same backwards and forwards.*

How can we evaluate this phrase to check if it is in fact a palindrome? Perhaps we can take the phrase and separate all of the characters apart and then iterate through each letter in one direction and compare it to its equivalent position in the opposite direction. We will utilize this logic again in additional applications Let's represent this logic in pseudo code.

```
# Initialize a variable called 'phrase' to hold the phrase
phrase = "A man, a plan, a canal: Panama." 
# Initialize a variable called 'letters' that holds all of the letters (a-z) 
letters = split(phrase) 
# Initialize a variable called 'phraseLength' 
phrase-length = length(letters)

# Iterate through each of the letters
for index->letter in letters:  
    # Check the current letter and its opposite for equivalency
    if letters[index] != letters[phrase-length-index]
        print "This is not a palindrome"
```        

We added a new convention here, a `for` loop.  This loop simply will iterate through each of the values in `letters`. Here `index` would be a number representing its location in the variable `letters`, and `letter` would be the actual value. The problem is this loop will print out a message if one of the characters does not equal its opposite. What it does not do is give us a clear answer whether or not the the inputted value is indeed a palindrome. Ideally we would like to see the outcome look like this:

```
print isPalindrome("french toast")
>>>     False
```
In this case the `isPalindrome()` function returned a conclusive boolean (true/false) value letting us know whether or not the inputted value is indeed a palindrome or not. Later on we will explore how to acheive this.

#### Prove if the given number is a prime number or not
*A prime number is one that is only divisible by one and itself.*

A very rudimentary way of solving this would be by multiplying all combinations of numbers from 1 until the given value and see if any of them equal the given value. This is obviously a very crude and timely method, but for small numbers should give us a valid answer none the less.
```
# Initialize a variable to hold the input
n = 52
# Iterate from 1 until 1-n
for x in range(1, n): 
    # Iterate from 1 until 1-n
    for y in range(1, n):
        # Evaluate if the product of the two values equals n    
        if x*y == n: 
            return False
    
return True
```
## Thinking Like an Engineer
Now that we have explored some logic problems. We have begun to understand the some of the kind of problems you will need to understand in the software development process. The next step is learning how to approach problems like these correctly.

The goal is to learn how to think like an engineer and instead of focusing on language specifics we will hope to best cover the guidelines of many of the technologies used in modern software applications

### The Unicorn of Technologies
There is no mystical technology that is best suited for all different circumstances. Every technology has its pros and cons and its area that it is best suited for.
This is why attempting to be the expert of all variations on a technology is not only impossible but the entirely wrong approach. When you learn best to think like an engineer and know the different options you may utilize, that puts you in the saddle ready to ride.
  
The different technology categories that we are going to deal with are:

* Operating Systems - The lowest level interface that your applications run on. The major operating system we will be using is POSIX or more specifically operating systems that run the Linux kernel. We me mention some additional OS's but we will not be focusing much on too much OS specific related data.

* Programming Languages - There are many programming languages. Some languages are limited to single OS's others are made to function on multiple operating systems. The two major branches of languages are those which are statically typed, and those which are dynamically typed.
    * A statically typed language is one that has it variables defined with specific types. Such languages include C, C++, Java, and most recently Go. There are many statically typed langauges each having their own merits and best use cases. There are plenty of technologies that may be your favorite to use but may no longer have a large active user community. Have a strong user community is very important to your grown and success in software engineering.
    * Dynamically typed languages allow for variables to be defined with different value types at run-time. We will explore a great deal more of the history of some languages and what advantages and disadvantages are present in each of the variances discussed.
* Databases
    * RDBMS - Relational database management system is type of database that is structured with tables and columns. Each entry represents a row of the table. RBDMS is very performant for structured data that has relationships with other data models.
    * Key Value Store - A key value store is a simple databases that uses a 'key' and corresponding 'value' like a map or dict.
    * Document Store - A newer type of database that has emerged that handles nested documents. You can query its data with query selectors. Describing the data.
* Messaging Protocols
* Transport Protocols