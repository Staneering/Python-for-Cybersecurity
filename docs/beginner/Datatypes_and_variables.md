
---

### **2. Variables and Data Types** (`docs/beginner/02_variables_and_data_types.md`)


# Variables and Data Types

In this section, you'll learn about the core building blocks of Python: **variables** and **data types**. Understanding these concepts is essential because they allow you to store and manipulate the data that your cybersecurity tools and scripts will work with.

## Variables in Python

A **variable** is a name that refers to a value stored in memory. You can think of variables as "containers" that hold data.

### Example:
```python
# Variables for storing different types of data
ip_address = "192.168.1.1"  # IP address of a server (str)
open_ports = [22, 80, 443]  # List of open ports on a server (list)
is_vulnerable = True  # Boolean indicating whether the system is vulnerable (bool)
username = "admin"  # Username for a login attempt (str)
```

### Variable Naming Rules:
- Variable names must start with a letter or underscore (`_`).
- They can contain letters, numbers, and underscores, but not spaces.
- Variable names should be descriptive and follow Python’s naming conventions.

---

## Data Types in Python

Python has several built-in data types, and understanding them is crucial for manipulating data effectively.

1. **Integers (`int`)**: Whole numbers, e.g., `5`, `100`, `-32`.
2. **Floating Point Numbers (`float`)**: Decimal numbers, e.g., `3.14`, `0.99`, `-12.5`.
3. **Strings (`str`)**: Text, enclosed in quotes, e.g., `"Hello"`, `'Python'`.
4. **Booleans (`bool`)**: Represents `True` or `False`.

### Example:
```python
# Example of different data types in a cybersecurity context

# An integer representing the number of failed login attempts
failed_login_attempts = 3  # int

# A float representing the percentage of traffic on a network
traffic_percentage = 23.5  # float

# A string for the username used in authentication
username = "admin"  # str

# A boolean flag indicating whether a port is open
is_port_open = True  # bool
```

### Common Use Case in Cybersecurity:
- **Integers**: Used for counting things like **failed login attempts**, **network traffic**, or **number of vulnerabilities detected**.
- **Floats**: Often used to represent **percentage values**, such as the percentage of packets lost in a network or **network bandwidth usage**.
- **Strings**: Represent various **textual data**, including **usernames**, **IP addresses**, or **error messages**.
- **Booleans**: Commonly used to represent true/false states like **whether a server is vulnerable**, **whether a port is open**, or if an **authentication attempt is successful**.

---

## Type Conversion

In Python, you can convert between different data types. This is useful when you need to work with data in different formats.

### Example:
```python
# Convert string to integer for numerical operations
ip_address_string = "192"
ip_address_int = int(ip_address_string)  # Convert to integer
print(ip_address_int + 8)  # Output: 200

# Convert integer to string for easier display in user interface
failed_attempts = 3
failed_attempts_str = str(failed_attempts)  # Convert to string
print("Failed login attempts: " + failed_attempts_str)  # Output: Failed login attempts: 3
```

### Cybersecurity Example:
Converting data types can be especially useful when handling user input. For instance, when processing login attempts or **password strength validation**, you might need to validate if input is a number or check if a string contains certain characters.

---

## Summary

Now you know how to store and manipulate different types of data using variables. These skills are foundational for developing cybersecurity scripts and tools that interact with networks, servers, and user data.

---

## Next Lesson

Once you're comfortable with variables and data types, proceed to the next lesson: [Control Structures](03_control_structures.md).
```

---

### Explanation of Changes:
1. **Cybersecurity Context**: The examples are specifically tailored to common cybersecurity tasks. For instance, **failed login attempts**, **traffic percentage**, and **port status** are all directly relevant to security operations and network monitoring.
2. **Variable Naming**: The examples show how variables can store data like **IP addresses**, **open ports**, and **vulnerability flags**, which are essential for security scripting.
3. **Type Conversion**: We included examples showing how to convert between data types, which is a common task when handling **user input** or **network data** (e.g., converting string IP addresses into integers for calculations).

---

