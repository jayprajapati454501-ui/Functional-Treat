# 📊 Data Analyzer and Transformer

A menu-driven **Python Data Analyzer and Transformer** program that allows users to enter, analyze, filter, sort, and summarize a dataset. The project demonstrates important Python programming concepts including **built-in functions, recursion, lambda functions, sorting, returning multiple values, global variables, and `**kwargs`**.

---

## 📌 Project Overview

This project is a console-based Python application for working with a list of numerical data.

The program provides eight menu options:

1. Input Data
2. Display Data Summary
3. Calculate Factorial
4. Filter Data by Threshold
5. Sort Data
6. Display Dataset Statistics
7. View Tracked Metrics Information
8. Exit Program

These options are implemented in the main program menu.

---

## 🎯 Objectives

The main objectives of this project are:

* To accept numerical data from the user.
* To load default sample data when required.
* To calculate basic dataset statistics.
* To use Python built-in functions such as `len()`, `min()`, `max()`, and `sum()`.
* To demonstrate recursion using factorial calculation.
* To demonstrate a lambda function for filtering data.
* To sort data in ascending or descending order.
* To return multiple values from a function.
* To demonstrate the use of `**kwargs`.
* To maintain global dataset metrics.

---

## 🛠️ Technologies Used

| Technology / Concept   | Purpose                              |
| ---------------------- | ------------------------------------ |
| Python                 | Main programming language            |
| List                   | Stores numerical dataset             |
| Built-in Functions     | Calculates basic statistics          |
| Recursion              | Calculates factorial                 |
| Lambda Function        | Filters values using a threshold     |
| `sort()`               | Sorts dataset                        |
| Multiple Return Values | Returns statistics together          |
| `**kwargs`             | Displays tracked metrics dynamically |
| Global Variables       | Tracks dataset count and average     |
| Functions              | Organizes program functionality      |

---

## 📂 Dataset

The program stores numerical values in the global `DATASET` list.

```python
DATASET = []
```

The program can either accept numbers entered by the user or load the default sample dataset:

```python
[34, 12, 56, 78, 43, 21, 90]
```

The input function converts valid numeric strings into integers before storing them.

---

## ✨ Features

### 1. Input Data

The user can choose between:

* Entering their own numbers
* Loading the default sample data

Example:

```text
--- Step 1: Input Data ---
1. Enter your own numbers
2. Load default sample data
```

After data is entered, the program automatically updates the global metrics.

---

### 2. Display Data Summary

The program calculates and displays:

* Total number of elements
* Minimum value
* Maximum value
* Sum of all values
* Average value

It uses Python built-in functions such as `len()`, `min()`, `max()`, and `sum()`.

Example:

```text
Data Summary:
 - Total elements: 7
 - Minimum value: 12
 - Maximum value: 90
 - Sum of all values: 334
 - Average value: 47.71
```

---

### 3. Calculate Factorial Using Recursion

The project demonstrates recursion through the `calculate_factorial()` function.

```python
def calculate_factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * calculate_factorial(n - 1)
```

The function repeatedly calls itself until it reaches the base case.

Example:

```text
Enter a number to calculate its factorial: 30
Factorial of 30 is: 265252859812191058636308480000000
```

---

### 4. Filter Data Using Lambda Function

The program uses a lambda function to identify values greater than or equal to a user-provided threshold.

```python
is_above_threshold = lambda x: x >= threshold
```

The filtered values are then stored in a separate list.

Example:

```text
Enter a threshold value to filter out data above this value: 23

Filtered Data (values >= 23):
[34, 56, 78, 43, 90]
```

---

### 5. Sort Data

The program allows the user to choose:

1. Ascending order
2. Descending order

The dataset is sorted using Python's `sort()` method.

Example:

```text
Choose sorting option:
1. Ascending
2. Descending

Enter your choice: 2

Sorted Data in Descending Order:
[90, 78, 56, 43, 34, 21, 12]
```

---

### 6. Display Dataset Statistics

The function `get_multiple_values()` calculates four values:

* Minimum
* Maximum
* Sum
* Average

These values are returned together from one function.

The returned values are then unpacked:

```python
minimum, maximum, total_sum, average = get_multiple_values()
```

This demonstrates how Python functions can return multiple values.

Example:

```text
Dataset Statistics:
 - Minimum value: 12
 - Maximum value: 90
 - Sum of all values: 334
 - Average value: 47.71
```

---

### 7. View Tracked Metrics Using `**kwargs`

The project demonstrates the use of variable keyword arguments with `**kwargs`.

```python
def dataset_summary_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f" - {key}: {value}")
```

The program passes the tracked dataset information dynamically to this function.

Example:

```text
Dataset Characteristics Summary:
 - total_tracked_elements: 7
 - computed_global_average: 47.71
```

---

## 🧠 Important Python Concepts

### Built-in Functions

The project uses:

```python
len(DATASET)
min(DATASET)
max(DATASET)
sum(DATASET)
```

These functions are used to calculate dataset statistics.

### Recursion

Factorial is calculated by a function calling itself:

```python
return n * calculate_factorial(n - 1)
```

### Lambda Function

Filtering uses:

```python
lambda x: x >= threshold
```

### Sorting

The List is sorted using:

```python
DATASET.sort()
```

or:

```python
DATASET.sort(reverse=True)
```

### Multiple Return Values

One function returns:

```python
return minimum, maximum, total_sum, average
```

### `**kwargs`

Keyword arguments are collected dynamically:

```python
def dataset_summary_kwargs(**kwargs):
```

### Global Variables

The program maintains:

```python
TOTAL_COUNT = 0
GLOBAL_MEAN = 0.0
```

These values track the number of dataset elements and the calculated global average.

---

## 🔄 Program Flow

```text
START
  ↓
Display Main Menu
  ↓
Choose an Option
  ↓
┌──────────────────────────────────┐
│ 1. Input Data                    │
│ 2. Display Data Summary          │
│ 3. Calculate Factorial            │
│ 4. Filter Data by Threshold      │
│ 5. Sort Data                     │
│ 6. Display Dataset Statistics    │
│ 7. View Tracked Metrics          │
│ 8. Exit Program                  │
└──────────────────────────────────┘
  ↓
Perform Selected Operation
  ↓
Return to Main Menu
  ↓
Exit
```

---

## 📋 Main Menu

```text
Main Menu:
1. Input Data
2. Display Data Summary (Built-in Functions)
3. Calculate Factorial (Recursion)
4. Filter Data by Threshold (Lambda Function)
5. Sort Data
6. Display Dataset Statistics (Return Multiple Values)
7. View Tracked Metrics Info (**kwargs)
8. Exit Program
```

The menu continuously runs inside a `while True` loop until the user selects option 8.

---

## 📊 Sample Dataset

```text
34, 12, 56, 78, 43, 21, 90
```

For this dataset:

| Statistic      | Result |
| -------------- | -----: |
| Total Elements |      7 |
| Minimum        |     12 |
| Maximum        |     90 |
| Sum            |    334 |
| Average        |  47.71 |

---

## 🔢 Sample Operations

### Filtering

For threshold `23`:

```text
Filtered Data:
[34, 56, 78, 43, 90]
```

### Descending Sort

```text
[90, 78, 56, 43, 34, 21, 12]
```

### Dataset Statistics

```text
Minimum value: 12
Maximum value: 90
Sum of all values: 334
Average value: 47.71
```

---

## ⚠️ Input Validation

The program checks whether numerical input contains valid digits when entering data and when calculating factorial. It also validates the threshold input before filtering.
If the user enters an invalid menu option, the program displays an error message and returns to the menu.

---

## ▶️ How to Run

### Step 1: Install Python

Install Python 3 on your computer.

### Step 2: Save the Program

Save the Python source file as:

```text
project_4.py
```

### Step 3: Open Terminal

Navigate to the folder containing the Python file.

### Step 4: Run the Program

```bash
python project_4.py
```

---

## 📁 Project Structure

```text
Data-Analyzer-and-Transformer/
│
├── project_4.py
├── README.md
└── screenshots/
    ├── input_data.png
    ├── data_summary.png
    ├── factorial.png
    ├── filter_data.png
    ├── sort_data.png
    └── metrics.png
```

---

## ✅ Advantages

* Simple menu-driven interface.
* Easy to understand and operate.
* Demonstrates multiple Python programming concepts.
* Provides useful numerical statistics.
* Supports ascending and descending sorting.
* Demonstrates recursion and lambda functions.
* Demonstrates multiple return values.
* Demonstrates dynamic keyword arguments using `**kwargs`.

## 🚀 Future Enhancements

The project could be improved by adding:

* CSV or JSON file storage.
* Data visualization using graphs and charts.
* Search and advanced filtering.
* Median and mode calculations.
* Standard deviation and variance.
* Database integration.
* A graphical user interface using Tkinter.
* Exporting analysis results to a report.

## 👨‍💻 Project Information

**Project Name:** Data Analyzer and Transformer
**Programming Language:** Python
**Application Type:** Console-Based Application
**Dataset Type:** Numerical Data
**Main Concepts:** Built-in Functions, Recursion, Lambda, Sorting, Multiple Return Values, Global Variables, `**kwargs`
