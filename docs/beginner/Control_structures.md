Great! Let's move on to the next topic: **Control Structures**.

---

### **3. Control Structures** (`docs/beginner/03_control_structures.md`)

```markdown
# Control Structures

Control structures are fundamental to programming because they allow you to manage the flow of your code. In this section, we’ll cover **conditional statements** and **loops**, both of which are commonly used in cybersecurity scripts to automate tasks, analyze data, and make decisions.

## Conditional Statements

Conditional statements allow you to execute certain code blocks based on conditions. This is important when making decisions, like checking if a port is open or if a password meets security criteria.

### Syntax:
```python
if condition:
    # Code to execute if condition is True
elif another_condition:
    # Code to execute if the second condition is True
else:
    # Code to execute if all conditions are False
```

### Example: Check if a Port is Open
In network security, it’s common to check if a port is open on a target system. We can use a simple `if` statement to check the port status.

```python
target_port = 80
if target_port == 80:
    print("Port 80 is open. It's commonly used for HTTP traffic.")
else:
    print("Port is closed.")
```

This example checks if the port is 80 (HTTP) and informs the user whether the port is open or closed.

### More Complex Conditional: Password Validation
In cybersecurity, we often validate passwords for security. For instance, checking if a password contains uppercase letters, numbers, and special characters:

```python
password = "Cyber$2025"

if len(password) >= 8 and any(char.isdigit() for char in password) and any(char.isupper() for char in password):
    print("Password is strong.")
else:
    print("Password is weak. Make sure it's at least 8 characters long, contains a number, and an uppercase letter.")
```

---

## Loops

Loops allow you to repeat a block of code multiple times. This is useful in tasks like scanning multiple IP addresses for vulnerabilities or testing multiple ports on a server.

### For Loop

A `for` loop iterates over a sequence (like a list or range) and executes a block of code for each item.

#### Example: Scan Multiple Ports
In a basic network scanning script, we might loop through a list of ports to check if they are open:

```python
ports = [22, 80, 443, 8080]
for port in ports:
    print(f"Checking port {port}...")
    # Here, you would add your code to check if the port is open
    # For example, using socket or other networking libraries
```

This loop iterates over each port in the `ports` list and performs a check on each one.

### While Loop

A `while` loop continues to execute as long as a condition is `True`. This is useful for tasks that need to run continuously, like checking a server for responses or monitoring a system for activity.

#### Example: Monitor Failed Login Attempts
You might want to continually monitor the number of failed login attempts until the threshold is met.

```python
failed_attempts = 0
while failed_attempts < 3:
    print("Attempting to log in...")
    failed_attempts += 1  # Simulate a failed login
    if failed_attempts >= 3:
        print("Account locked due to too many failed login attempts.")
        break  # Exit the loop when the condition is met
```

In this example, the loop continues until the number of failed login attempts reaches 3.

---

## Nested Loops and Conditions

You can also nest loops and conditionals inside each other to create more complex logic. This is particularly useful when dealing with multidimensional data or performing multiple checks.

### Example: Check Multiple Ports for Multiple Servers
In a scenario where you need to check multiple ports on multiple servers, you can use nested loops.

```python
servers = ["192.168.1.1", "192.168.1.2"]
ports = [22, 80, 443]

for server in servers:
    for port in ports:
        print(f"Scanning {server} on port {port}...")
        # Add code to check if the port is open on the server
```

This will loop over each server and check all the ports on each server.

---

## Summary

Control structures are essential for creating dynamic and responsive Python programs. They allow you to:
- **Make decisions** based on conditions (e.g., checking if a port is open or a password is strong).
- **Repeat actions** (e.g., scanning multiple ports or monitoring failed login attempts).
- **Combine conditions and loops** to handle more complex scenarios (e.g., scanning multiple servers for vulnerabilities).

---

