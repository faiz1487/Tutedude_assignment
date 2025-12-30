# Python Basics Assignment Report

## Student Information
- **Student Name:** Faizan Kaishar
- **Course / Module:** Python Basics
- **Topic:** Conditional Statements, Dictionary Operations, File Handling
- **Environment:** Linux (Ubuntu) – Python 3

---

## Objective
The objective of this assignment is to understand basic Python programming concepts, including:
- Conditional statements (if-else)
- Dictionary data structure
- File handling (read and write operations)
- Executing Python programs using Linux bash commands

---

## System Requirements
- **Operating System:** Linux (Ubuntu or similar)
- **Python Version:** Python 3.10.12
- **Text Editor:** vi
- **Terminal:** Bash

---

## Task 1: Grade Checker Program

### Description
This program takes a student’s score as input and prints the corresponding grade using conditional statements.

### Grading Criteria
- **90 and above:** A
- **80 – 89:** B
- **70 – 79:** C
- **60 – 69:** D
- **Below 60:** F

### Code
```python
score = int(input("Enter your score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

### Execution Command
```bash
python3 grade_checker.py
```

### Output
The program displays the grade based on the entered score.

---

## Task 2: Student Grades Management Using Dictionary

### Description
This program uses a dictionary to store student names and their grades. It allows users to:
- Add a new student
- Update an existing student’s grade
- Display all student records

### Code
```python
students = {}

while True:
    print("\n1. Add Student")
    print("2. Update Student Grade")
    print("3. Print All Students")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter student name: ")
        grade = input("Enter grade: ")
        students[name] = grade
        print("Student added successfully.")

    elif choice == "2":
        name = input("Enter student name to update: ")
        if name in students:
            grade = input("Enter new grade: ")
            students[name] = grade
            print("Grade updated successfully.")
        else:
            print("Student not found.")

    elif choice == "3":
        print("\nStudent Grades:")
        for name, grade in students.items():
            print(name, ":", grade)

    elif choice == "4":
        print("Exiting program.")
        break

    else:
        print("Invalid choice.")
```

### Execution Command
```bash
python3 student_grades.py
```

---

## Task 3: Write Data to a File

### Description
This program creates a text file and writes content into it using Python file handling methods.

### Code
```python
file = open("sample.txt", "w")
file.write("Hello, this is a sample text file.\n")
file.write("Python file handling is easy to learn.")
file.close()

print("Data written to file successfully.")
```

### Execution Command
```bash
python3 write_file.py
```

### Output
A file named `sample.txt` is created with the given content.

---

## Task 4: Read Data from a File

### Description
This program reads data from an existing text file and displays it on the terminal.

### Code
```python
file = open("sample.txt", "r")
content = file.read()

print("File Content:\n")
print(content)

file.close()
```

### Execution Command
```bash
python3 read_file.py
```

---

## Conclusion
This assignment helped in understanding fundamental Python concepts such as conditional logic, dictionaries, file handling, and executing Python programs using Linux bash commands. These basics are essential for building real-world automation and scripting solutions.

---

**E
