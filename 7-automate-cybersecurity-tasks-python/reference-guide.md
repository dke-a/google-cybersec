## Reference Guide: Python Concepts from Course 7

### Sections

- [Comments](#comments)
- [Conditional Statements](#conditional-statements)
- [Iterative Statements](#iterative-statements)
- [User-Defined Functions](#user-defined-functions)
- [Built-In Functions](#built-in-functions)
- [Importing Modules and Libraries](#importing-modules-and-libraries)
- [String Methods](#string-methods)
- [List Methods](#list-methods)
- [Additional Syntax for Working with Strings and Lists](#additional-syntax-for-working-with-strings-and-lists)
- [Regular Expressions](#regular-expressions)
- [File Operations](#file-operations)
- [Parsing](#parsing)

------

### Comments

- **#**
  Starts a single-line comment in Python. For example:

  ```python
  # Print approved usernames
  ```

  Indicates that the purpose of the following code is to print approved usernames.

- **""" (Documentation Strings)**
  Used for multi-line comments or documentation. For example:

  ```python
  """
  The estimate_attempts() function takes in a monthly
  login attempt total and a number of months and
  returns their product.
  """
  ```

### Conditional Statements

- **if**
  Starts a conditional statement. For example:

  ```python
  if device_id != "la858zn":
  if user in approved_list:
  ```

  Evaluates whether a condition is True.

- **elif**
  Introduces an additional condition after the `if` statement. For example:

  ```python
  elif status == 500:
  ```

  Evaluates the condition if the previous ones are False.

- **else**
  Provides an alternative action if all preceding conditions are False. For example:

  ```python
  
  else:
  ```

- **and**
  Requires both conditions to be True. For example:

  ```python
  if username == "bmoreno" and login_attempts < 5:
  ```

- **or**
  Requires at least one of the conditions to be True. For example:

  ```python
  if status == 100 or status == 102:
  ```

- **not**
  Negates a condition. For example:

  ```python
  
  if not account_status == "removed":
  ```

### Iterative Statements

- **for**
  Begins a for loop to iterate through a sequence. For example:

  ```python
  
  for username in ["bmoreno", "tshah", "elarson"]:
  for i in range(10):
  ```

- **while**
  Begins a while loop that continues as long as a condition is True. For example:

  ```python
  
  while login_attempts < 5:
  ```

- **break**
  Exits a loop prematurely.

- **continue**
  Skips the current iteration and continues with the next one.

### User-Defined Functions

- **def**
  Used to define a function. For example:

  ```python
  
  def greet_employee():
  def calculate_fails(total_attempts, failed_attempts):
  ```

- **return**
  Exits a function and returns a value. For example:

  ```python
  
  return fail_percentage
  ```

### Built-In Functions

- **print()**
  Outputs a value to the screen. For example:

  ```python
  
  print("login success")
  print(9 < 7)
  ```

- **type()**
  Returns the data type of an object. For example:

  ```python
  
  print(type(51.1))
  ```

- **range()**
  Generates a sequence of numbers. For example:

  ```python
  
  range(0, 5, 1)
  ```

- **max()**
  Returns the largest of its inputs. For example:

  ```python
  
  print(max(10, 15, 5))
  ```

- **min()**
  Returns the smallest of its inputs. For example:

  ```python
  
  print(min(10, 15, 5))
  ```

- **sorted()**
  Sorts elements in a list or other iterable. For example:

  ```python
  
  print(sorted([10, 15, 5]))
  ```

- **str()**
  Converts an object to a string. For example:

  ```python
  
  str(10)
  ```

- **len()**
  Returns the number of elements in an object. For example:

  ```python
  
  print(len("security"))
  ```

### Importing Modules and Libraries

- import

  Imports a module or library. For example:

  ```python
  
  import statistics
  from statistics import mean, median
  ```

### String Methods

- **.upper()**
  Converts a string to uppercase. For example:

  ```python
  
  print("Security".upper())
  ```

- **.lower()**
  Converts a string to lowercase. For example:

  ```python
  
  print("Security".lower())
  ```

- **.index()**
  Returns the index of the first occurrence of a substring. For example:

  ```python
  
  print("Security".index("c"))
  ```

### List Methods

- **.insert()**
  Inserts an element at a specific position in a list. For example:

  ```
  python
  
  
  Copy code
  username_list.insert(2,"wjaffrey")
  ```

- **.remove()**
  Removes the first occurrence of a specified element. For example:

  ```
  python
  
  
  Copy code
  username_list.remove("elarson")
  ```

- **.append()**
  Adds an element to the end of a list. For example:

  ```
  python
  
  
  Copy code
  username_list.append("btang")
  ```

- **.index()**
  Returns the index of the first occurrence of an element in a list. For example:

  ```
  python
  
  
  Copy code
  print(username_list.index("tshah"))
  ```

### Additional Syntax for Working with Strings and Lists

- **+ (concatenation)**
  Combines two strings or lists. For example:

  ```
  python
  
  
  Copy code
  device_id = "IT" + "nwp12"
  users = ["elarson", "bmoreno"] + ["tshah", "btang"]
  ```

- **[] (bracket notation)**
  Extracts elements from a string or list using indices. For example:

  ```
  python
  
  
  Copy code
  print("h32rb17"[0:3])
  print(username_list[2])
  ```

### Regular Expressions

- **re.findall()**
  Returns a list of matches for a regular expression. For example:

  ```
  python
  
  
  Copy code
  import re
  re.findall("a53", "a53-32c .E")
  ```

- **\w**
  Matches any alphanumeric character or underscore. For example:

  ```
  python
  
  
  Copy code
  re.findall("\w", "a53-32c .E")
  ```

- **.**
  Matches any character except a newline. For example:

  ```
  python
  
  
  Copy code
  re.findall(".", "a53-32c .E")
  ```

- **\d**
  Matches any digit. For example:

  ```
  python
  
  
  Copy code
  re.findall("\d", "a53-32c .E")
  ```

- **\s**
  Matches any whitespace character. For example:

  ```
  python
  
  
  Copy code
  re.findall("\s", "a53-32c .E")
  ```

- **.**
  Matches a literal period. For example:

  ```
  python
  
  
  Copy code
  re.findall("\.", "a53-32c .E")
  ```

- **+**
  Matches one or more occurrences of the preceding element. For example:

  ```
  python
  
  
  Copy code
  re.findall("\w+", "a53-32c .E")
  ```

- ------

  Matches zero or more occurrences of the preceding element. For example:

  ```
  python
  
  
  Copy code
  re.findall("\w*", "a53-32c .E")
  ```

- **{ }**
  Matches a specific number of occurrences of the preceding element. For example:

  ```
  python
  
  
  Copy code
  re.findall("\w{3}", "a53-32c .E")
  ```

### File Operations

- **with**
  Manages file opening and ensures proper resource management. For example:

  ```
  python
  
  
  Copy code
  with open("logs.txt", "r") as file:
  ```

- **open()**
  Opens a file. For example:

  ```
  python
  
  
  Copy code
  with open("login_attempts.txt", "r") as file:
  with open("update_log.txt", "w") as file:
  with open(import_file, "a") as file:
  ```

- **as**
  Assigns an alias to the file object. For example:

  ```
  python
  
  
  Copy code
  with open("logs.txt", "r") as file:
  ```

- **.read()**
  Reads the contents of a file as a string. For example:

  ```
  python
  
  
  Copy code
  file_text = file.read()
  ```

- **.write()**
  Writes a string to a file. For example:

  ```
  python
  
  
  Copy code
  file.write("jrafael")
  ```

### Parsing

- .split()

  Splits a string into a list. For example:

  ```
  python
  
  
  Copy code
  approved_users = "elarson,bmoreno,tshah".split(",")
  removed_users = "wjaffrey jsoto abernard".split()
  ```