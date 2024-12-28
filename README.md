# Python-Assignment-4
This  Assignment explains about the functions in Python
# 1.What does the len() function do in Python?
# Write a code example using len() to find the length of a list.

# The len() function in Python is used to determine the length (number of items) of an object.
# It is commonly used with sequences (like strings, lists, tuples) and collections (like dictionaries and sets).
# len() function is versatile and widely used for working with iterable objects in Python.
l1=[1,2,3,4,5,6,7,8,9,10]
print(len(l1))

# 2.Write a Python function greet(name) that takes a person's name as input and prints "Hello, [name]!"
def greet():
    name=input('enter your name:')
    print('"Hello,',name,'!"')
greet()

# 3.Write a Python function find_maximum(numbers) that takes a list of integers and returns the maximum value without using the built-in max() function.
# Use a loop to iterate through the list and compare values.
def find_maximum(numbers):
    numbers=[3, 5, 7, 2, 8, -1, 4]
    if not numbers:
        return None
    Maximum_value = numbers[0]
    for num in numbers:
        if num> Maximum_value:
            Maximum_value=num
    return Maximum_value
numbers=[3, 5, 7, 2, 8, -1, 4]
print("Maximum value:", find_maximum(numbers))


# 4.Explain the difference between local and global variables in a Python function.
# Write a program where a global variable and a local variable have the same name and show how Python differentiates between them.

# A global variable is defined outside any function and can be accessed and modified throughout the program, including inside functions (with certain conditions).
# Global variables are used when multiple functions or parts of the program need to share and modify the same data.

# A local variable is defined inside a function and can only be accessed within that function.
# Local variables are typically used to store temporary data that is specific to the function's operation.

output=5000#global variable
def result():
    output=10000#local variable
    print("value of output inside the function (local variable):",output)
result()#fn call
print("value of output outside the function (Global variable):",output)

# 5.Create a function calculate_area(length, width=5) that calculates the area of a rectangle.
# If only the length is provided, the function should assume the width is 5.
# Show how the function behaves when called with and without the width argument.

def calculate_area(length, width=5):
    area=length*width
    return area
result1=calculate_area(10) # without width argument ,default=5
result2=calculate_area(10,3) #with width argument
print("Area of a rectangle:",result1)
print("Area of a rectangle:",result2)
