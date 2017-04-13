---
layout: page
title:  "Python 101"
day: 1
---

# Python Fundamentals

## Download the .ipynb file
You can download the notebook file [here](Week1/Python101.ipynb).

## Variables & Arithmetic
Whatever you're coding, you will need places to store different types of data. The most basic way to store data is through variables. 


```python
# Here, we are declaring a variable with the name x and storing it with the integer value 10
x = 10 
```


```python
#You can check what the value of a variable is by simply printing it in the following manner
print x
```

    10



```python
#You can also declare multiple variables as shown:
x,y = 1,2
print x,y
```

    1 2



```python
# You can store differnt types of data in variables, as shown in the examples below.

y = 2.3 #This is called a float type, where you can store decimals
print y

z = "This is z!" #You can also store strings in a variable, by putting them in between single or double quotations
print z
```


```python
#It is easy to concatenate (or combine) strings with each other

hello = "Hello"
world = "World"
helloworld = hello + " " + world
print helloworld
```


You can also perform arithmetic using numerical variables. 

### Addition



```python
10 + 10
```


```python
x = 1
print x + 2

x= x+3
print x
```

### Multiplication
To multiply numbers or variables in Python, you can simply use this symbol: *


```python
x = 5 

print x*2
```

### Division
For division, Python uses /


```python
x = 10
print x / 5
```


```python
#Note that Python will only give back integers unless otherwise specified.

print 10/3 #Even though the answer should be a decimal (called a float in Python), it gives you back integers
```


```python
print 10.0/3 # You need to specify by diving 10.0, not 10.
```


```python
# If you are working with floating variables, you can declare them as following:

x = 10.0

#Have an integer you want to convert to a float?

y = 1
print y

y = float(y)
print y

```

### Exponents

Raising numbers to a power is easy in Python. Simply use the double asterix: **


```python
5**10
```


```python
x = 2
y = 8
print x**y
print y**x
```

## Lists, Tuples & Dictionaries

These are the other three major types of data structures in Python. 



```python
# Lists are just a collection of objects (strings/integers/floats) and are declared using []

empty_list = [] #This is how you declare an empty list

x = [1,2,3]
print x

y = ["a","b","c"]
print y
```

    [1, 2, 3]
    ['a', 'b', 'c']



```python
# Lists have an index that can be used to get items from it
 
x[0] # Note that the first element is not at index 1, but at index 0. In Python, indexes go from 0 -->(n-1)
```


```python
# You can also slice things out of a list by using the indexes as follows

x[0:2] #Note that the last index is not included. 
```


```python
y[1:3]
```


```python
#Items in a list can also be changed. For example, if you want to change the second element in the list x to 4:

x[1]=4 
x
```




    [1, 4, 3]




```python
#You can also add to lists by using the .append() function

x.append(5)
x
```




    [1, 4, 3, 4]




```python
# You can also change/remove elements from a list. 

x = [1,2,3] 
x[0] = 0 #This changes the item at the 0th index of the list to 0. 
```


```python
#Removing items is simple! You have two ways of acheiving that. 

y = ['a','b','c']

del y[1] #Removes the item at the 1st index

y.pop(0) #The pop function also does the same thing, but has different syntax and way of doing it. 
```


```python
# Lastly, you can also check to see the length of a list by running the len function.
len(x)
```




    4




```python
#Tuples on the other hand are immutable. They are immutable lists declared using ()

x = (1,2,3)
x
```


```python
# What happens when you append a tuple?
x.append(4)
```


```python
# Dictionaries are key value pair stores. These are declared using {}

fruits= {'Bananas':10, 'Strawberries':5, 'Pineapple':20}
fruits['Pineapple']
```




    20




```python
#Add a dictionary entry very simply

fruits['Apples'] = 8
fruits
```




    {'Apples': 8, 'Bananas': 10, 'Pineapple': 20, 'Strawberries': 5}




## Booleans & Conditionals
Booleans are an important part of coding. They are like a switch and can only have two values: True or False. They are very useful in conditional statements that we will be discussing next. But first, 


```python
x = 11 #Assignment is not the same as the equal to sign in Python
x == 6
```




    False




```python
x/5 != 2 
```




    True




```python
x/5.0 ==2 
```




    False




```python
#If statements are very useful ways to fork the code. If x is true then you do something, otherwise, 
#do something else.
if x <=20:
    x += 2
    print x
else:
    print x
```

    13



```python
# You can also combine if statements in the following ways:
x = 3
if x ==1 or x==2:
    print "x is 1 or 2"
else: 
    print "x is neither 1 nor 2"
```


```python
#Another way to use if statements are by adding more clauses using the elif statement. (elif = else-if)
x=5
if x ==1:
    print "x is 1"
elif x==2:
    print "x is 2"
elif x==3:
    print "x is 3"
else:
    print "x is not 1, 2 or 3"
```

#### Exercise
Write a set of conditional statements that check to see if n is divisible whole by 2. If it is, then print "n is even". Otherwise, print "n is odd". I've started off the code for you below!

Hint: % is the modulo operator


```python
n = int(raw_input("Enter a number: ")) # This command simply asks the user to enter an integer value first 
# Add your conditionals below    

```

## Loops

Loops are a very useful way of repeating something over and over again, with some conditionals on when to break them.There are two kinds of loops: for and while. 
For loops are usually used for iterating through lists and doing something with every iteration.
While loops are often used to accumulate additions in a variable. 



```python
# An example of the for-loop. Iterate through the numbers 1-11. What do you think this function does?
x = [1,2,3,4,5,6,7,8,9,10]

for i in x:
    if i % 2 == 0: 
        print i
```


```python
for i in "string":
    print i 
```


```python
count = 0 #While loops are different! You need to make sure that you break them. 

while count < 10:
    print "The count is: ",count
    count += 1
```


```python
#An example of a while loop going backwards
count = 10

while count >0:
    print count
    count = count -1
else: 
    print "Launch!"
```

## Functions
Functions are an integral part of Python where you can make seperate modules, and call them whenever they are needed. Let's go through the syntax first, and then step-by-step, make a function for finding if a number is a whole square.



```python
from math import sqrt

def whole_square_checker(n): #sqrt is the name, and it takes an argument, n
    if sqrt(n).is_integer()==True: #Line checks whether sqrt(n) is an integer by calling the built in is_integer func
        print "n is a whole square, and its square root is",sqrt(n)
    else:
        print "n is not a whole square"
        
whole_square_checker(100)
```

The return command is also very important to use with functions. It can be passed into other functions to solve more complicated issues.

Below, let's make a function that will return the number of whole squares between any 1, and a number the user provides. This will use our whole_square_checker function, though we will have to modify it first. 


```python
def whole_square_check(n): #Change the name from the function above a little
    if sqrt(n).is_integer() == True: 
        return True
    else:
        return False
    
l = []    
def whole_squares_in(x):
    for i in range(1,x):
        if whole_square_check(i) == True:
           l.append(i)
    return l

x = int(raw_input("Enter the end of your range: "))


print whole_squares_in(x)
```


### Exercises

a. Construct a function that returns all the divisors of the number the user inputs as a list.


b. **Challenge:** Write a function for finding out the factorial of a number that the user inputs. 

c. **Challenge:** Take an input from the user. Write a function that returns a list of all primes between 1 and that number. 


```python

```


```python

```
