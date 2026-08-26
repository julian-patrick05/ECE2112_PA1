# **ECE-2112-PA-1**
#### Julian Patrick C. Herrera | 2ECE-C
*This repository contains three programming problems which covers **Module 1 - Base Computing with Python**.*
**Objectives:**
1. use basic Python functions, operators, and string operations;
2. manipulate strings using indexing, slicing, and built-in string methods;
3. apply sequence unpacking to manipulate the elements of a list; and
4. construct simple Python functions that return a specified result.
## **A. Word Rotation Problem**
Create a function that moves the **first character** of the string to the end while keeping all remaining characters in their original order and preserves the capitalization of every character.
The following functions used in this problem are:
-  **String Indexing** : ```text[1:]``` - Used to **access** individual characters within a string based on their numerical position. String indexing uses zero-based indexing, with **[0]** as the first position in a string rather than **[1]**.

-  **String Slicing** : ```text[0]``` - Used to **extract** all characters from the starting index until the end of the string.
### **Code**
```python
def rotate_word(text):
    return text[1:] + text[0]
```
### Outputs
```python
rotate_word("python")
```
Output: ```'ythonp'```
```python
rotate_word("logic")
```
Output: ```'ogicl'```
```python
rotate_word("Code")
```
Output: ```'odeC'```
```python
rotate_word("A")
```
Output: ```'A'```
## **B. Username Builder Problem**
Create a function named **make_username()** that accepts two strings: **first_name** and **last_name**.

The function must:
- convert all letters to lowercase;
- remove all spaces from the first name;
- remove all spaces from the last name; and
- join the processed first and last names using one period (.).

Functions used in this problem are:
- ```.lower()```- replaces all characters in the string into **lowercase**.

- ```.replace(" ", "")``` - **replaces** old instances of a specified string with a new one.
### **Code**
```python
def make_username(first_name, last_name):
    lower_first = first_name.lower().replace(" ", "")
    lower_last = last_name.lower().replace(" ", "")

    return lower_first + "." + lower_last
```
### **Outputs**
```python
make_username("Ada", "Lovelace")
```
Output: ```'ada.lovelace'```
```python
make_username("Alan", "Turing")
```
Output: ```'alan.turing'```
```python
make_username("Ana Maria", "De Leon")
```
Output: ```'anamaria.deleon'```
## **C. Bookend Swap Problem**
Create a function named **swap_bookends()** that accepts a list containing at least two elements. Unpack the list into three variables:

- first – the first element;
- middle – a list containing everything between the first and last elements; and
- last – the last element.

Use **extended sequence unpacking** in the following form:
- ```*first,* **middle, last = items*```
### Code
```python
def swap_bookends(items):
    first, *middle, last = items

    return [last] + middle + [first]
```
### Outputs
```python
swap_bookends([1, 2, 3, 4, 5, 6])
```
Output: ```[6, 2, 3, 4, 5, 1]```
```python
swap_bookends(["red", "green", "blue"])
```
Output: ```['blue', 'green', 'red']```

```python
swap_bookends([8, 3])
```
Output: ```[3, 8]```

To view and test the code:
- Download ```'Programming Assignment 1.ipynb'``` that is located in this repository
- Open via Jupyter Notebook
- Click 'Run'
  
**README File Version History:**

```August 26, 2026``` - Initial README.md output uploaded
