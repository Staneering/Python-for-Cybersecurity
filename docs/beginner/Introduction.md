
---

### **1. Introduction to Python for Cybersecurity** (`docs/beginner/01_introduction_to_python.md`)


# Introduction to Python for Cybersecurity

Python is an essential programming language for cybersecurity professionals. It's widely used for writing scripts to automate security tasks, create cybersecurity tools, and analyze data. In this section, we will introduce Python, help you set up your development environment, and get you started with writing basic Python code.

## Setting Up Your Environment

Before we start coding, let's set up Python and the libraries you will need.

### 1. Install Python
Download and install Python from the official [Python website](https://www.python.org/downloads/). Follow the installation instructions, and make sure to check the box to add Python to your system’s PATH during installation.

### 2. Install Libraries
For our cybersecurity-related projects, we will need some libraries. To install them, open your terminal or command prompt and run:

```bash
pip install pycryptodome requests beautifulsoup4 scapy
```

These libraries are essential for tasks such as encryption, web scraping, and network analysis. Here's a quick overview of what they'll be used for:
- **pycryptodome**: For encryption and decryption.
- **requests**: For sending HTTP requests (often used in web-based security tasks).
- **beautifulsoup4**: For web scraping and analyzing HTML content.
- **scapy**: For network packet manipulation and analysis.

## Writing and Running Python Code

Python code can be written in any text editor, but using an IDE (Integrated Development Environment) like **VS Code** or **PyCharm** will make things easier. After writing your code, you can run it in the terminal.

### Example: Write Your First Python Script

Let's write a simple Python script to get started. This script will fetch the title of a website — a task commonly performed in **web security analysis**.

```python
import requests

# Get the title of a webpage
url = "https://www.example.com"
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    print(f"Website Title: {response.text.split('<title>')[1].split('</title>')[0]}")
else:
    print(f"Failed to retrieve {url}")
```

### What This Code Does:
- It uses the `requests` library to send an HTTP GET request to a website (in this case, "https://www.example.com").
- If the request is successful (status code `200`), it parses the HTML content to extract the title of the page.
- This is just a simple example, but similar techniques are used in security tasks like **web scraping for vulnerability analysis** or **scraping threat intelligence** from websites.

### Running Python Code
You can run Python scripts from the terminal by navigating to the directory where your script is saved and typing:

```bash
python hello_world.py
```

This will execute the script and print the output.

---


