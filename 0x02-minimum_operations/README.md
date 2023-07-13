How to use the Python min function?
In this tutorial, we learn how to use the Python min function. This is one of the many functions in Python, like max(), len(), abs(), etc. We can use them without importing a module or a library.

Table of contents
What does the min() function do in Python?
Syntax of the Python min() function
Using the min() function with iterables
Using the min() function with multiple arguments
Closing thoughts

What does the min() function do in Python?
Python’s min() function is primarily used to return the smallest item in an iterable. Furthermore it is also used to find the smallest item between two or more parameters or arguments. Example: print(min(2, -1.0, 30, -9))

Syntax for the Python min() function
The min() function is written in two forms:

1. Syntax to find the smallest item in an iterable
min(iterable, *iterables, key, default)
a. iterable - an iterable; can be list, tuple, set, dictionary, etc.
b. *iterables (optional) - any number of iterables; can be more than one.
c. key (optional) - the key function where the iterables are passed and comparison is performed based on its returned value.
d. default(optional) - default value if the given iterable is empty.

2. Syntax to find the smallest item between two or more objects
min(arg1, arg2, *args, key)
a. arg1 - an object; can be numbers, strings, etc.
b. arg2 - an object; can be numbers, strings, etc.
c. *args (optional) - any number of objects.
d. key (optional) - key function where each argument is passed, and comparison is performed based on its return value.
Using the min() function with iterables
Finding the smallest item in a string using the Python min() function
If the elements in an iterable are strings, the earliest element in alphabetical order is returned as the output.

Input:
languages = ["Spanish", "English", "French", "Italian"]
small_string = min(languages)
       
print("The smallest string in languages is:", small_string)
Output:
The smallest string in languages is: English
Finding the smallest item in a list using the Python min() function
Here we will take the input as a list with integer values in it. And using the min() function we will find the smallest value integer in the list.

Input:
num = [3, -2, 1, 15, 10, 0.6]
small_num = min(num)
print("The smallest number is:", small_num)
       
Output:
The smallest number is: -2
Finding the smallest key and value in dictionaries using the Python min() function
For dictionaries, we can find both the smallest key and the smallest value pair individually.

Input:
sample_dict = {1: 2, 3: 4, -5: 6, -7: 8}

# finding the smallest key 
key_one = min(sample_dict)
print("The smallest key in sample_dict is:", key_one)   

# finding the key whose value is the smallest
key_two = min(sample_dict, key = lambda k: sample_dict[k])
print("The key with the smallest value in sample_dict:", key_two)  

# getting the smallest value
print("The smallest value found is:", sample_dict[key_two])    
        
Output:
The smallest key in sample_dict is: -7
The key with the smallest value in sample_dict: 1
The smallest value found is: 2
The second time we used the min() function, we passed a lambda function to the key parameter. The function returns the values of dictionaries. So the key having the smallest value is computed instead of the keys themselves.

Using the min() function with multiple arguments
Here, we have called on the min() function while passing multiple arguments to be evaluated. Python’s min() function evaluates each element and then returns the smallest value.

Input:
print(min(2, -1.0, 30, -9)) 
print(min("f", "l", "e", "x", "i"))
print(min(7.14, -1.12, 7.66))
Output:
-9
e
-1.12
Points to note:
When we pass an empty iterator, a ValueError exception is raised. To avoid this, we can pass the default parameter.
print(min([]))  # here the empty iterable causes ValueError
# The solution
print(min([], default=0)) #negating the error with default value
If more than one iterator is passed then the smallest item from the given iterators is returned.
#Input:
list_one = [11,12,13]
list_two = [2, 4, 6, 8, 10, 12]
min_val = min(list_one, list_one, key = len)
print("The minimum value : ", min_val) 
  
#Output:
The minimum value :  [11, 12, 13]
In this example, the minimum value in terms of the length of the list is returned because the key=len is applied
