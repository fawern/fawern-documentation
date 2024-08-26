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

code = assistant.generate_code(prompt)

print(code)
```

This will generate Python code for a snake game using Pygame based on the given prompt.
To write the generated code to a file, you can use the following code:

```python
assistant.write_code_to_file(path='./')
```

This will write the generated code to a file named `generated_file_name.py` in the current directory.
You can use run_generated_code() method to run the generated code:

```python
assistant.run_generated_code()
```

This will run the generated code using the Python interpreter.

### CodeAnalyzer

Here's an example of how to use the **CodeAnalyzer** feature to analyze and refactor Python code:

```python
from fawern import CodeAnalyzer

analyzer = CodeAnalyzer()

code = """
def add_numbers(a, b):
    return a + b

print(add_numbers(5, '10'))
"""

# Analyze the code
analysis = analyzer.analyze_code(code)
print(analysis)

# Find and fix syntax errors
fixed_code = analyzer.find_syntax_errors(code)
print(fixed_code)

# Suggest optimizations
optimizations = analyzer.suggest_optimizations(code)
print(optimizations)
```

This will analyze the given Python code, find syntax errors, and suggest optimizations to improve the code.

### CodeFormatter

Format Python code according to PEP8 standards:

```python
from fawern import CodeFormatter

formatter = CodeFormatter()

code = """
def addNumbers(a,b):
    return a + b
"""

# Format the code
formatted_code = formatter.format_code(code)
print(formatted_code)

```

This will format the given Python code according to PEP8 standards.

### ErrorLogAnalyzer

Log and analyze Python errors, providing suggestions for fixes:

```python
from fawern import ErrorLogAnalyzer

error_analyzer = ErrorLogAnalyzer()

# Log an error
error_message = "TypeError: unsupported operand type(s) for +: 'int' and 'str'"
error_analyzer.log_error(error_message)

# Analyze logged errors
analysis = error_analyzer.analyze_errors()
print(analysis)
```

This will log the given error message and analyze it to provide suggestions for fixes.

### CodeReviewer

Review Python code and provide feedback on structure, clarity, and quality:

```python
from fawern import CodeReviewer

reviewer = CodeReviewer()

code = """
def add_numbers(a, b):
    return a + b
"""

# Review the code
review = reviewer.review_code(code)
print(review)
```

This will review the given Python code and provide feedback on its structure, clarity, and quality.

### DocumentationGenerator

Generate detailed docstrings and inline comments for Python code:

```python
from fawern import DocumentationGenerator

doc_generator = DocumentationGenerator()

code = """
def add_numbers(a, b):
    return a + b
"""

# Generate docstrings and comments
documentation = doc_generator.generate_docstrings(code)
print(documentation)
```

This will generate detailed docstrings and inline comments for the given Python code.

### ConvertToPython

Convert code from other programming languages to Python:

```python
from fawern import ConvertToPython

converter = ConvertToPython()

java_code = """
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
"""

# Convert Java code to Python
python_code = converter.convert_code(java_code)
print(python_code)
```

This will convert the given Java code to Python code.

### CodeVisualizer

Generate visual representations such as flowcharts or class diagrams for Python code:

```python
from fawern import CodeVisualizer

visualizer = CodeVisualizer()

code = """
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"
"""

# Visualize the code
visualization = visualizer.visualize_code(code)
print(visualization)

```

This will generate a class diagram for

### BugFixer

Automatically identify and fix bugs in Python code:

```python
from fawern import BugFixer

bug_fixer = BugFixer()

code = """
def add_numbers(a, b):
    return a + b

print(add_numbers(5, '10'))
"""

# Fix bugs in the code
fixed_code = bug_fixer.fix_bugs(code)
print(fixed_code)
```

This will automatically identify and fix bugs in the given Python code.

### UnitTestGenerator

Generate unit tests for Python code to ensure correctness:

```python
from fawern import UnitTestGenerator

test_generator = UnitTestGenerator()

code = """
def add_numbers(a, b):
    return a + b
"""

# Generate unit tests for the code
unit_tests = test_generator.generate_tests(code)
print(unit_tests)
```

This will generate unit tests for the given Python code to ensure its correctness.

## Contributing

Contributions are welcome! But fawern is not public yet. We will make it public soon.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- This project was inspired by the need for AI-powered tools to assist developers in various aspects of software development.
