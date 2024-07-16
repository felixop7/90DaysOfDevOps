# Day 11: Python Basics and Automation Fundamentals

## Daily Log

**Date:** June 29, 2024

Today, I continued my 90 Days of DevOps journey by exploring Python basics and automation fundamentals. Python is a versatile language widely used in DevOps for scripting, automation, and various other tasks. This day’s activities focused on understanding Python's core concepts and applying them to automate simple tasks.

## Key Concepts

### Basics of Python

Python is a high-level, interpreted programming language known for its readability and ease of use. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming. Python is often used in DevOps for automation, scripting, and configuration management due to its simplicity and extensive libraries.

## Tasks

### 1. Learned about variables, data types (strings, integers, lists, dictionaries), and basic operations

#### Variables and Data Types

In Python, variables are used to store data, which can be of different types:

- **Strings**: Text data enclosed in quotes (e.g., `"Hello, World!"`).
- **Integers**: Whole numbers (e.g., `42`).
- **Lists**: Ordered collections of items (e.g., `[1, 2, 3]`).
- **Dictionaries**: Key-value pairs (e.g., `{"name": "Alice", "age": 30}`).

#### Basic Operations

- Arithmetic operations: Addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`), and modulo (`%`).
- String operations: Concatenation (`+`), repetition (`*`), and slicing (`[]`).

#### Example:

```python
# Variables
name = "Alice"
age = 30
fruits = ["Apple", "Banana", "Cherry"]
person = {"name": "Alice", "age": 30}

# Basic operations
sum = 10 + 5
product = 4 * 3
greeting = "Hello, " + name
first_fruit = fruits[0]
```

### 2. Practiced creating and manipulating variables, and performing arithmetic operations

#### Example:

```python
# Creating variables
a = 10
b = 20

# Performing arithmetic operations
sum = a + b
difference = a - b
product = a * b
quotient = b / a

# Printing results
print(f"Sum: {sum}")
print(f"Difference: {difference}")
print(f"Product: {product}")
print(f"Quotient: {quotient}")
```

### File Handling and Automation

File handling is crucial for automation tasks in Python, such as reading from and writing to files. This is often used for logging, configuration management, and data processing.

### 1. Implemented a Python script to read a text file, count occurrences of specific words, and print results

#### Example:

```python
# Read a text file and count word occurrences

# Function to count occurrences of specific words in a file
def count_words(file_path, words_to_count):
    with open(file_path, 'r') as file:
        text = file.read().lower()
        word_count = {word: text.count(word) for word in words_to_count}
    return word_count

# Specify the file path and words to count
file_path = 'example.txt'
words_to_count = ['python', 'devops', 'automation']

# Count words and print results
word_count = count_words(file_path, words_to_count)
print(word_count)
```

### 2. Created a script to write data to a new file based on user input

#### Example:

```python
# Write user input to a new file

# Function to write user input to a file
def write_to_file(file_path):
    with open(file_path, 'w') as file:
        while True:
            user_input = input("Enter text (type 'exit' to quit): ")
            if user_input.lower() == 'exit':
                break
            file.write(user_input + '\n')

# Specify the file path
file_path = 'output.txt'

# Write to the file
write_to_file(file_path)
```

### Practice Git Integration

Git integration is an essential skill for DevOps engineers, enabling version control, collaboration, and automation of deployment processes.

### 1. Successfully cloned a Git repository using Python

#### Example:

```python
import os

# Clone a Git repository
repository_url = "https://github.com/your-repo.git"
os.system(f"git clone {repository_url}")
```

### 2. Automated committing and pushing changes to a remote repository with a Python script

#### Example:

```python
import os

# Define Git commands
repository_path = "/path/to/your/repo"
commit_message = "Automated commit"

# Change directory to the repository path
os.chdir(repository_path)

# Stage changes, commit, and push to the remote repository
os.system("git add .")
os.system(f"git commit -m '{commit_message}'")
os.system("git push")
```

## Reflection

Today’s tasks enhanced my understanding of Python and its applications in automation. I practiced basic Python concepts, file handling, and Git integration, which are essential skills for a DevOps engineer. Python's simplicity and powerful libraries make it a valuable tool for scripting and automating routine tasks in DevOps.

### References:

- [Python Official Documentation](https://docs.python.org/3/)
- [GeeksforGeeks: Python Basics](https://www.geeksforgeeks.org/python-programming-language/)
- [Automating Some Git Commands with Python](https://www.geeksforgeeks.org/automating-some-git-commands-with-python/)

---

**Happy Learning! 🚀**

Roshan Sahani
