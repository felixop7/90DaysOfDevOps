# Day 12: Intermediate Python Concepts for Automation 🐍

## Daily Log

**Date:** June 30, 2024

Today, I delved deeper into Python by exploring intermediate concepts essential for automation. These concepts include functions and modules, error handling and debugging, and networking and APIs. Mastering these topics is crucial for writing robust and efficient automation scripts in a DevOps environment.

## Key Concepts

### Functions and Modules

Functions in Python are blocks of reusable code designed to perform a single, related action. Modules are files containing Python code (functions, classes, variables) that can be imported and used in other scripts, promoting code reusability and organization.

## Tasks

### 1. Defined a function to calculate the factorial of a number and tested it with different inputs

#### Example:

```python
# Define a function to calculate the factorial of a number
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

# Test the function with different inputs
print(f"Factorial of 5: {factorial(5)}")
print(f"Factorial of 7: {factorial(7)}")
```

### 2. Created a module containing functions for basic math operations (addition, subtraction, multiplication)

#### math_operations.py:

```python
# Define basic math operations in a module
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b
```

#### main.py:

```python
# Import the math_operations module and test its functions
import math_operations as mo

print(f"Addition of 3 and 5: {mo.add(3, 5)}")
print(f"Subtraction of 10 and 4: {mo.subtract(10, 4)}")
print(f"Multiplication of 2 and 6: {mo.multiply(2, 6)}")
```

### Error Handling and Debugging

Error handling in Python is done using try-except blocks, allowing graceful handling of exceptions. Debugging tools like `pdb` or IDEs help identify and fix logical errors in the code.

### 1. Modified an existing script to handle exceptions gracefully (e.g., file not found, division by zero)

#### Example:

```python
# Handle exceptions gracefully

try:
    # Attempt to open a non-existent file
    with open('non_existent_file.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("Error: File not found.")

try:
    # Attempt to divide by zero
    result = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero.")
```

### 2. Debugged a script using pdb or an IDE to identify and fix logical errors

#### Example:

```python
# Debugging a script using pdb
import pdb

def faulty_function(a, b):
    pdb.set_trace()
    result = a + b
    result = result / (a - b)
    return result

# Test the function with inputs that cause an error
faulty_function(5, 5)
```

### Networking and APIs

Networking and APIs are crucial for automating interactions with web services and integrating various systems. Python's `requests` library simplifies making HTTP requests and handling responses.

### 1. Implemented a script to make HTTP GET requests using Python's requests library

#### Example:

```python
import requests

# Make an HTTP GET request
response = requests.get('https://jsonplaceholder.typicode.com/posts')

# Print the response status code and content
print(f"Status Code: {response.status_code}")
print(f"Response Content: {response.json()}")
```

### 2. Created a script to interact with a mock REST API (e.g., fetch data, update records)

#### Example:

```python
import requests

# URL of the mock REST API
api_url = 'https://jsonplaceholder.typicode.com/posts'

# Fetch data (GET request)
response = requests.get(api_url)
posts = response.json()
print("Fetched Posts:")
for post in posts[:5]:
    print(post)

# Update a record (PUT request)
update_data = {
    'id': 1,
    'title': 'Updated Title',
    'body': 'Updated body content',
    'userId': 1
}
response = requests.put(f"{api_url}/1", json=update_data)
print(f"Update Response: {response.json()}")
```

## Reflection

Today's tasks enhanced my understanding of intermediate Python concepts essential for automation. I practiced defining and using functions and modules, handling errors gracefully, debugging scripts, and working with APIs. These skills are crucial for writing robust and efficient automation scripts in a DevOps environment.

---

**Happy Learning! 🚀**

Roshan Sahani

---

### References:

- [Python Official Documentation](https://docs.python.org/3/)
- [GeeksforGeeks: Python Functions](https://www.geeksforgeeks.org/functions-in-python/)
- [Requests: HTTP for Humans](https://requests.readthedocs.io/en/latest/)
