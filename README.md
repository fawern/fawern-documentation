# fawern

**fawern** is a Python library designed to assist developers with various AI-powered tools for code generation, analysis, refactoring, and more. It utilizes advanced models to provide a wide range of functionalities, from generating Python code based on prompts to analyzing and fixing code, generating documentation, and even converting code from other languages to Python.

## Features

- **ChatPython:** Generate Python code based on a given input prompt.
- **CodeAnalyzer:** Analyze, refactor, and optimize Python code.
- **CodeFormatter:** Format Python code according to PEP8 standards.
- **ErrorLogAnalyzer:** Log and analyze Python errors, providing suggestions for fixes.
- **CodeReviewer:** Review Python code and provide feedback on structure, clarity, and quality.
- **DocumentationGenerator:** Generate detailed docstrings and inline comments for Python code.
- **ConvertToPython:** Convert code from other programming languages to Python.
- **CodeVisualizer:** Generate visual representations such as flowcharts or class diagrams for Python code.
- **BugFixer:** Automatically identify and fix bugs in Python code.
- **UnitTestGenerator:** Generate unit tests for Python code to ensure correctness.

## PyPi Package Link

Please check the package on PyPi to get the latest version and more information about the package.
[https://pypi.org/project/fawern/](https://pypi.org/project/fawern/)

## Installation

You can install Fawern using pip:

```bash
pip install fawern
```

## Usage

### ChatPython

Generate Python code based on a prompt:

```python
from fawern import ChatPython

assistant = ChatPython()

prompt = "Create a snake game using Pygame in Python. The snake should move with the arrow keys, grow when it eats food, and the game should end if it collides with the walls or itself. Display the current score during gameplay and the final score when the game ends."

code = assistant.generate_code(prompt, run_code=True)

print(code)
```

This will generate Python code for a snake game and write it to a file named related to the prompt. The code will be executed, and the output will be displayed.

### CodeAnalyzer

Here's an example of how to use the **CodeAnalyzer** feature to analyze and refactor Python code:

```python
from fawern import CodeAnalyzer

analyzer = CodeAnalyzer()

code = """
def process_data(data):
    result = []
    for i in range(len(data)):
        if data[i] % 2 == 0:
            result.append(data[i] * 2)
    return result

data = [1, 2, 3, 4, 5]
print(process_data(data))
"""

# Analyze the code for potential improvements
analysis = analyzer.analyze_code(code)
print("Analysis Report:\n", analysis)

# Fix detected issues and suggest improvements
fixed_code = analyzer.find_syntax_errors(code)
print("\nFixed Code:\n", fixed_code)

optimizations = analyzer.suggest_optimizations(fixed_code)
print("\nOptimized Code:\n", optimizations)
```

This will analyze the given Python code, find syntax errors, and suggest optimizations to improve the code.

### CodeFormatter

Format Python code according to PEP8 standards:

```python
from fawern import CodeFormatter

formatter = CodeFormatter()

code = """
def   calculateArea(   length,  width ) :
    return  length   *width

a =   5
b =  10
print  ( calculateArea  (a,  b ) )
"""

# Format the code
formatted_code = formatter.format_code(code)
print("Formatted Code:\n", formatted_code)
```

This will format the given Python code according to PEP8 standards.

### ErrorLogAnalyzer

Log and analyze Python errors, providing suggestions for fixes:

```python
from fawern import ErrorLogAnalyzer

error_analyzer = ErrorLogAnalyzer()

# Log an error from a web application
error_message = """
Traceback (most recent call last):
  File "/app.py", line 22, in <module>
    app.run()
  File "/flask/app.py", line 940, in run
    run_simple(host, port, self, **options)
TypeError: 'str' object is not callable
"""

# Analyze logged errors and get suggestions
analysis = error_analyzer.analyze_errors(error_message)
print("Error Analysis:\n", analysis)
```

This will log an error message from a web application, analyze the logged errors, and provide suggestions for fixes.

### CodeReviewer

Review Python code and provide feedback on structure, clarity, and quality:

```python
from fawern import CodeReviewer

reviewer = CodeReviewer()

code = """
import requests
from bs4 import BeautifulSoup

def scrape_website(url):
    response = requests.get(url)
    soup = BeautifulSoup(response.content, 'html.parser')
    titles = soup.find_all('h2')
    for title in titles:
        print(title.get_text())
"""

# Review the code
review = reviewer.review_code(code)
print("Code Review:\n", review)
```

This will review the given Python code and provide feedback on its structure, clarity, and quality.

### DocumentationGenerator

Generate detailed docstrings and inline comments for Python code:

```python
from fawern import DocumentationGenerator

doc_generator = DocumentationGenerator()

code = """
class Calculator:
    def add(self, a, b):
        return a + b

    def subtract(self, a, b):
        return a - b

    def multiply(self, a, b):
        return a * b

    def divide(self, a, b):
        if b == 0:
            return 'Error: Division by zero'
        return a / b
"""

# Generate docstrings and inline comments
documentation = doc_generator.generate_docstrings(code)
print("Generated Documentation:\n", documentation)
```

This will generate detailed docstrings and inline comments for the given Python code.

### ConvertToPython

Convert code from other programming languages to Python:

```python
from fawern import ConvertToPython

converter = ConvertToPython()

cpp_code = """
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 10;
    int sum = a + b;
    cout << "Sum: " << sum << endl;
    return 0;
}
"""

# Convert C++ code to Python
python_code = converter.convert_code(cpp_code)
print("Converted Python Code:\n", python_code)
```

This will convert the given Java code to Python code.

### CodeVisualizer

Generate visual representations such as flowcharts or class diagrams for Python code:

```python
from fawern import CodeVisualizer

visualizer = CodeVisualizer()

code = """
class Shape:
    def __init__(self, color):
        self.color = color

    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, color, width, height):
        super().__init__(color)
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, color, radius):
        super().__init__(color)
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius
"""

# Visualize the class hierarchy
visualization = visualizer.visualize_code(code)
print("Class Diagram:\n", visualization)
```

This will generate a class diagram for

### BugFixer

Automatically identify and fix bugs in Python code:

```python
from fawern import BugFixer

bug_fixer = BugFixer()

code = """
def divide_numbers(a, b):
    return a / b

print(divide_numbers(10, 0))
"""

# Fix bugs in the code
fixed_code = bug_fixer.fix_bugs(code)
print("Fixed Code:\n", fixed_code)
```

This will automatically identify and fix bugs in the given Python code.

### UnitTestGenerator

Generate unit tests for Python code to ensure correctness:

```python
from fawern import UnitTestGenerator

test_generator = UnitTestGenerator()

code = """
def multiply(a, b):
    return a * b
"""

# Generate unit tests for the code
unit_tests = test_generator.generate_tests(code)
print("Generated Unit Tests:\n", unit_tests)
```

This will generate unit tests for the given Python code to ensure its correctness.

## Contributing

Contributions are welcome! But fawern is not public yet. We will make it public soon.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- This project was inspired by the need for AI-powered tools to assist developers in various aspects of software development.
