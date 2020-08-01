# python

## variables

```python

## Print is a function in python3
print("This line will be printed.")

## standard indentation requires four spaces
x = 1
if x == 1:
    #indented four spaces
    print("x is 1.")

## To define an integer, use the following syntax:
myint = 7
print(myint)

#define integer as float
myfloat = 7.0
print(myfloat) 
#returns 7.0

myfloat = float(7)
print(myfloat) 
#returns 7.0

# Not every str() can be turned into float() or int(), but anything can be turned into str()

## Strings are defined either with a single quote or a double quotes.
mystring = 'hello'
print(mystring)
#returns hello

mystring = "hello"
print(mystring)
#returns hello

one = 1
two = 2
three = one + two
print(three)

hello = "hello"
world = "world"
helloworld = hello + " " + world
print(helloworld)

## Assignments can be done on more than one variable "simultaneously" on the same line like this (comma acts as spaces)

first, last = 'lindsay', 'shen'
print(first,last)
#returns lindsay shen

print(first,'is','awesome',last)
#returns lindsay is awesome shen

## only the same types of functions can be added together
one = 1
two = 2
hello = "hello"

print(str(one) + str(two) + hello)
#returns 12hello


# check what type the variable is using isinstance
mystring = "hello"
myfloat = 10.0
myint = 20

# testing code
if mystring == "hello":
    print("String: %s" % mystring)
if isinstance(myfloat, float) and myfloat == 10.0:
    print("Float: %f" % myfloat)
if isinstance(myint, int) and myint == 20:
    print("Integer: %d" % myint)
    #%d is a placeholder than can replace any word/number; %:what comes after is to replace %d

# This prints out "Hello, John!"
name = "John"
print("Hello, %s!" % name)

# This prints out "John is 23 years old."
name = "John"
age = 23
print("%s is %d years old." % (name, age))

## %s (tuple for string; can turn list into string as well); %f (for float); %d (for integer)
# Any object which is not a string can be formatted using the %s operator as well. The string which returns from the "repr" method of that object is formatted as the string. For example:

# This prints out: A list: [1, 2, 3]
mylist = [1,2,3]
print("A list: %s" % mylist)


# This prints out -> i have 3 dogs 
num_dog = 3
num_cat = 7 

print('i have %s dogs ' % num_dog)
print('i have %s dogs ' % (num_dog)) #if you have more than one thing to replace, you need to add a (); if only one thing, it will work w/wo a ()
print('i have ' + str(num_dog) + ' dogs')

###
%s - String (or any object with a string representation, like numbers)

%d - Integers

%f - Floating point numbers

%.<number of digits>f - Floating point numbers with a fixed amount of digits to the right of the dot.

%x/%X - Integers in hex representation (lowercase/uppercase)
###

##List can contain any type of variable, and they can contain as many variables as you wish.
mylist = []
mylist.append(1)
mylist.append(2)
mylist.append(3)
print(mylist[0]) # prints 1
print(mylist[1]) # prints 2
print(mylist[2]) # prints 3
#returns
#1
#2
#3

print(mylist[0],mylist[1],mylist[2])
#returns 1 2 3

# prints out 1,2,3
for x in mylist:
    print(x)
#returns
#1
#2
#3

mylist = [1,2,3]
print(mylist[0])
#returns 1

## In this exercise, you will need to add numbers and strings to the correct lists using the "append" list method. You must add the numbers 1,2, and 3 to the "numbers" list, and the words 'hello' and 'world' to the strings variable.

You will also have to fill in the variable second_name with the second name in the names list, using the brackets operator []. Note that the index is zero-based, so if you want to access the second item in the list, its index will be 1.
numbers = []
strings = []
names = ["John", "Eric", "Jessica"]

# write your code here
numbers.append(1)
numbers.append(2)
numbers.append(3)

strings.append("hello")
strings.append("world")

second_name = names[1]

# this code should write out the filled arrays and the second name in the names list (Eric).
print(numbers)
print(strings)
print("The second name on the names list is %s" % second_name)

#$%.2f means float with 2 decimals after integer; which prints out the same result as $%s
#$%s is the best solution here because it will return the correct result no matter types (i.e., if it is "53.44", a string, then $%.2f wouldn't work because you cannot change string into float)
data = ("John", "Doe", 53.44)
format_string = "Hello %s %s has $%.2f"
print(format_string % data)

format_string = "Hello %s %s has $%s"
print(format_string % data)



#returns 
    #[1, 2, 3]
    #['hello', 'world']
    #The second name on the names list is Eric

## List can be joined with the addition operators
even_numbers = [2,4,6,8]
odd_numbers = [1,3,5,7]
all_numbers = odd_numbers + even_numbers
print(all_numbers)
#returns [1, 3, 5, 7, 2, 4, 6, 8]

## multiplication operator can also forms repeating list sequence
print([1,2,3] * 3)
#returns [1, 2, 3, 1, 2, 3, 1, 2, 3]

## There are multiple ways to combine two lists
x_list = [x] 
y_list = [y] 

big_list = [*x_list , *y_list]

#or
big_list = x_list + y_list

## That prints out 4, because the location of the first occurrence of the letter "o" is 4 characters away from the first character. Notice how there are actually two o's in the phrase - this method only recognizes the first.
astring = "Hello world!"
print(astring.index("o"))
## That prints out 3 because it would count all the lower case 'L"s in the string
astring = "Hello world!"
print(astring.count("l"))

## That prints out "lo w"; []means slicing, in this case, it's slice from index 3 to 7, excluding 7.
astring = "Hello world!"
print(astring[3:7])

# this prints out the exact same result; This is extended slice syntax. The general form is [start:stop:step]. 
print(astring[3:7:1])
# This prints the characters of string from 3 to 7 skipping one character. This prints out "l"
print(astring[3:7:2])

## Reverse string, this prints out "!dlrow olleH"
astring = "Hello world!"
print(astring[::-1])

## This is used to determine whether the string starts with something or ends with something, respectively. 
astring = "Hello world!"
print(astring.startswith("Hello")) #True
print(astring.endswith("asdfasdfasdf")) #False

# ['Hello', 'world!']
afewwords = astring.split(" ")
print(afewwords)

## The standard Python indentation is 4 spaces, although tabs and any other space size will work, as long as it is consistent. 
## Here is an example for using Python's "if" statement using code blocks:
statement = False
another_statement = True
if statement is True:
    # do something
    pass
elif another_statement is True: # else if
    # do something else
    pass
else:
    # do another thing
    pass

## Notice that variable assignment is done using a single equals operator "=", whereas comparison between two variables is done using the double equals operator "==". 
x = 2
if x == 2:
    print("x equals two!")
else:
    print("x does not equal to two.")

x = [1,2,3]
y = [1,2,3]
print(x == y) # Prints out True
print(x is y) # Prints out False

## "if l:" here means if list L, in other words, if list L is not empty, print 5. L here is empty, so it would only print out 100
l = []
l2= [1,2]

if l:
  print(5)
if l2:
  print(100)

# change this code to make if statements true
number = 16
second_number = None #or you can put an empty list []
first_array = [1,2,3]
second_array = [1,2]

if number > 15:
    print("1")

if first_array: #if first_array is not empty
    print("2")

if len(second_array) == 2:
    print("3")

if len(first_array) + len(second_array) == 5:
    print("4")

if first_array and first_array[0] == 1: #if first_array is not empty and if first_array's index 0 is 1
    print("5")

if not second_number: #means if second_number is not not empty (which is it's empty)
    print("6")

## for loop
# Prints out the numbers 0,1,2,3,4
for x in range(5):
    print(x)

# Prints out 3,4,5
for x in range(3, 6):
    print(x)

# Prints out 3,5,7
for x in range(3, 8, 2):
    print(x)

## while loop
# Prints out 0,1,2,3,4
count = 0
while count < 5:
    print(count)
    count += 1  # This is the same as count = count + 1

## "break" and "continue" statements
# Prints out 0,1,2,3,4

count = 0
while True:
    print(count)
    count += 1
    if count >= 5:
        break #used to exit a for/while loop

# Prints out only odd numbers - 1,3,5,7,9
for x in range(10):
    # Check if x is even
    if x % 2 == 0:
        continue #used to skip the current block and return to for/while loop
    print(x)

## tuple is immutable, more secured ()
## list: you can change items in lists []

## When the loop condition of "for" or "while" statement fails then code part in "else" is executed. If break statement is executed inside for loop then the "else" part is skipped. Note that "else" part is executed even if there is a continue statement.
# Prints out 0,1,2,3,4 and then it prints "count value reached 5"

count=0
while(count<5):
    print(count)
    count +=1
else:
    print("count value reached %d" %(count))

# Prints out 1,2,3,4
for i in range(1, 10):
    if(i%5==0):
        break
    print(i)
else:
    print("this is not printed because for loop is terminated because of break but not due to fail in condition")

## Loop through and print out all even numbers from the numbers list in the same order they are received. Don't print any numbers that come after 237 in the sequence.

numbers = [
    951, 402, 984, 651, 360, 69, 408, 319, 601, 485, 980, 507, 725, 547, 544,
    615, 83, 165, 141, 501, 263, 617, 865, 575, 219, 390, 984, 592, 236, 105, 942, 941,
    386, 462, 47, 418, 907, 344, 236, 375, 823, 566, 597, 978, 328, 615, 953, 345,
    399, 162, 758, 219, 918, 237, 412, 566, 826, 248, 866, 950, 626, 949, 687, 217,
    815, 67, 104, 58, 512, 24, 892, 894, 767, 553, 81, 379, 843, 831, 445, 742, 717,
    958, 609, 842, 451, 688, 753, 854, 685, 93, 857, 440, 380, 126, 721, 328, 753, 470,
    743, 527]

# solution 1
for number in numbers:
    if number == 237:
        break

    if number % 2 == 1: #this means if number is odd, skip)
        continue

    print(number) #print function here is not tabbed because it is irrelevant to the if statements above

# solution 2
for number in numbers:
    if number == 237:
        break
    if number % 2 == 0: #if number is even, print this number
        print(number)

## Functions in python are defined using the block keyword "def", followed with the function's name as the block's name.
# functions may return a value to the caller (return); may also receive arguments (variables passed fromn the caller to the function)
# Define our 3 functions
def my_function():
    print("Hello From My Function!")

def my_function_with_args(username, greeting):
    print("Hello, %s , From My Function!, I wish you %s"%(username, greeting))

def sum_two_numbers(a, b):
    return a + b

# print(a simple greeting)
 my_function()

#prints - "Hello, John Doe, From My Function!, I wish you a great year!"
 my_function_with_args("John Doe", "a great year!")

# after this line x will hold the value 3!
 x = sum_two_numbers(1,2)
 print(x)

## Printing and returning are completely different concepts. 
# print is a function you call.
# When a return statement is reached, Python will stop the execution of the current function, sending a value out to where the function was called. 
# Use return when you want to send a value from one point in your code to another.



```

