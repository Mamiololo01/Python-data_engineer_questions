# Python Data Engineering Questions

This repository contains a collection of coding problems designed to test and improve your data engineering skills using Python. The problems cover various topics such as control flows, basic SQL operations, string manipulations, data structures, and more.

## Table of Contents
- [Introduction](#introduction)
- [Problems](#problems)
  - [Problem 2: Odd or Even](#problem-2-odd-or-even)
  - [Problem 3: Basic Arithmetic](#problem-3-basic-arithmetic)
  - [Problem 4: Division](#problem-4-division)
  - [Problem 5: Squares](#problem-5-squares)
  - [Problem 6: Leap Year](#problem-6-leap-year)
  - [Problem 7: Print Series](#problem-7-print-series)
  - [Problem 8: Runner-Up Score](#problem-8-runner-up-score)
  - [Problem 9: Second Lowest Grade](#problem-9-second-lowest-grade)
  - [Problem 10: Average Marks](#problem-10-average-marks)
  - [Problem 11: List Operations](#problem-11-list-operations)
  - [Problem 12: Hash Tuple](#problem-12-hash-tuple)
  - [Problem 13: Swap Case](#problem-13-swap-case)
  - [Problem 14: Split and Join](#problem-14-split-and-join)
  - [Problem 15: Full Name](#problem-15-full-name)
  - [Problem 16: Mutate String](#problem-16-mutate-string)
  - [Problem 17: Substring Count](#problem-17-substring-count)
  - [Problem 18: String Validation](#problem-18-string-validation)
  - [Problem 19: Text Wrap](#problem-19-text-wrap)
  - [Problem 20: Door Mat Design](#problem-20-door-mat-design)
  - [Problem 21: Number Formatting](#problem-21-number-formatting)
  - [Problem 22: Alphabet Rangoli](#problem-22-alphabet-rangoli)
  - [Problem 23: Capitalize Names](#problem-23-capitalize-names)
  - [Problem 24: Shoe Shop](#problem-24-shoe-shop)
  - [Problem 25: Polar Coordinates](#problem-25-polar-coordinates)
  - [Problem 31: Average Plant Height](#problem-31-average-plant-height)
  - [Problem 32: Supermarket](#problem-32-supermarket)
  - [Problem 33: Integer Division](#problem-33-integer-division)
  - [Problem 34: Day Finder](#problem-34-day-finder)
  - [Problem 35: Word Occurrences](#problem-35-word-occurrences)
  - [Problem 36: Time Delta](#problem-36-time-delta)
  - [Problem 37: Newspaper Subscriptions](#problem-37-newspaper-subscriptions)
  - [Problem 38: Subset Check](#problem-38-subset-check)
  - [Problem 39: Superset Check](#problem-39-superset-check)
  - [Problem 40: Polynomial Verification](#problem-40-polynomial-verification)
  - [Problem 41: Regex Split](#problem-41-regex-split)
  - [Problem 42: String Sort](#problem-42-string-sort)
  - [Problem 43: Fibonacci Cubes](#problem-43-fibonacci-cubes)

## Introduction

This repository is a collection of Python programming problems that focus on various aspects of data engineering. Each problem is designed to help you practice and improve your coding skills in Python, covering topics such as control flows, basic SQL operations, string manipulations, and data structures.

## Problems

### Problem 2: Odd or Even
```python
n = int(input())
if n % 2 == 1:
    print("Weird")
elif n % 2 == 0 and n >= 2 and n <= 5:
    print("Not Weird")
elif n % 2 == 0 and n >= 6 and n <= 20:
    print("Weird")
elif n % 2 == 0 and n > 20:
    print("Not Weird")

Problem 3: Basic Arithmetic

a = int(input())
b = int(input())
print(a + b)
print(a - b)
print(a * b)

Problem 4: Division

a = int(input())
b = int(input())
print(a // b)
print(a / b)

Problem 5: Squares

n = int(input())
for i in range(n):
    print(i ** 2)

Problem 6: Leap Year

def is_leap(year):
    leap = False
    if year % 400 == 0:
        leap = True
    elif year % 100 == 0:
        leap = False
    elif year % 4 == 0:
        leap = True
    return leap

Problem 7: Print Series

n = int(input())
for i in range(1, n+1):
    print(i, end="")

Problem 8: Runner-Up Score

n = int(input())
arr = list(map(int, input().split()))
first = max(arr)
runner_up = max([x for x in arr if x != first])
print(runner_up)

Problem 9: Second Lowest Grade

students = []
for _ in range(int(input())):
    name = input()
    score = float(input())
    students.append([name, score])

second_lowest = sorted(list(set([score for name, score in students])))[1]
second_lowest_students = sorted([name for name, score in students if score == second_lowest])
for student in second_lowest_students:
    print(student)

Problem 10: Average Marks

n = int(input())
student_marks = {}
for _ in range(n):
    name, *line = input().split()
    scores = list(map(float, line))
    student_marks[name] = scores
query_name = input()
scores = student_marks[query_name]
print("{:.2f}".format(sum(scores) / len(scores)))

Problem 11: List Operations

result = []
for _ in range(int(input())):
    cmd = input().split()
    if cmd[0] == "insert":
        result.insert(int(cmd[1]), int(cmd[2]))
    elif cmd[0] == "print":
        print(result)
    elif cmd[0] == "remove":
        result.remove(int(cmd[1]))
    elif cmd[0] == "append":
        result.append(int(cmd[1]))
    elif cmd[0] == "sort":
        result.sort()
    elif cmd[0] == "pop":
        result.pop()
    elif cmd[0] == "reverse":
        result.reverse()

Problem 12: Hash Tuple

n = int(input())
integer_list = map(int, input().split())
t = tuple(integer_list)
print(hash(t))

Problem 13: Swap Case

def swap_case(s):
    return s.swapcase()

Problem 14: Split and Join

def split_and_join(line):
    return "-".join(line.split())

Problem 15: Full Name

def print_full_name(a, b):
    print(f"Hello {a} {b}! You just delved into python.")

Problem 16: Mutate String

def mutate_string(string, position, character):
    return string[:position] + character + string[position+1:]

Problem 17: Substring Count

def count_substring(string, sub_string):
    count = 0
    for i in range(len(string) - len(sub_string) + 1):
        if string[i:i+len(sub_string)] == sub_string:
            count += 1
    return count

Problem 18: String Validation

s = input()
print(any(c.isalnum() for c in s))
print(any(c.isalpha() for c in s))
print(any(c.isdigit() for c in s))
print(any(c.islower() for c in s))
print(any(c.isupper() for c in s))

Problem 19: Text Wrap

import textwrap

def wrap(string, max_width):
    return textwrap.fill(string, max_width)

Problem 20: Door Mat Design

N, M = map(int, input().split())
pattern = [('.|.' * (2*i + 1)).center(M, '-') for i in range(N//2)]
print('\n'.join(pattern + ['WELCOME'.center(M, '-')] + pattern[::-1]))

Problem 21: Number Formatting

def print_formatted(number):
    width = len(bin(number)[2:])
    for i in range(1, number + 1):
        print(f"{i:{width}d} {i:{width}o} {i:{width}X} {i:{width}b}")

Problem 22: Alphabet Rangoli

def print_rangoli(size):
    import string
    alpha = string.ascii_lowercase
    L = []
    for i in range(size):
        s = "-".join(alpha[i:size])
        L.append((s[::-1] + s[1:]).center(4*size-3, "-"))
    print('\n'.join(L[::-1] + L[1:]))


def solve(s):
    return ' '.join(word.capitalize() for word in s.split(' '))

Problem 24: Shoe Shop

from collections import Counter

X = int(input())
sizes = Counter(map(int, input().split()))
N = int(input())
earnings = 0

for _ in range(N):
    size, price = map(int, input().split())
    if sizes[size]:
        earnings += price
        sizes[size] -= 1

print(earnings)

Problem 25: Polar Coordinates

import cmath
z = complex(input())
print(abs(z))
print(cmath.phase(z))

Problem 31: Average Plant Height

def average(array):
    return sum(set(array)) / len(set(array))

Problem 32: Supermarket

from collections import OrderedDict

items = OrderedDict()
for _ in range(int(input())):
    *item, price = input().split()
    item = ' '.join(item)
    items[item] = items.get(item, 0) + int(price)

for item, price in items.items():
    print(item, price)
Public code references from 21 repositories
Problem 33: Integer Division
Python
for _ in range(int(input())):
    a, b = input().split()
    try:
        print(int(a) // int(b))
    except ZeroDivisionError as e:
        print("Error Code:", e)
    except ValueError as e:
        print("Error Code:", e)

Problem 34: Day Finder

import calendar

month, day, year = map(int, input().split())
print(calendar.day_name[calendar.weekday(year, month, day)].upper())

Problem 35: Word Occurrences

from collections import defaultdict

d = defaultdict(list)
n, m = map(int, input().split())

for i in range(n):
    d[input()].append(i + 1)

for _ in range(m):
    print(' '.join(map(str, d[input()])) or -1)

Problem 36: Time Delta

from datetime import datetime

def time_delta(t1, t2):
    fmt = "%a %d %b %Y %H:%M:%S %z"
    return str(int(abs((datetime.strptime(t1, fmt) - datetime.strptime(t2, fmt)).total_seconds())))

Problem 37: Newspaper Subscriptions

eng = int(input())
eng_subs = set(map(int, input().split()))
fr = int(input())
fr_subs = set(map(int, input().split()))
print(len(eng_subs.intersection(fr_subs)))

Problem 38: Subset Check

for _ in range(int(input())):
    a, set_a = int(input()), set(input().split())
    b, set_b = int(input()), set(input().split())
    print(set_a <= set_b)

Problem 39: Superset Check

A = set(input().split())
print(all(A > set(input().split()) for _ in range(int(input()))))

Problem 40: Polynomial Verification

x, k = map(int, input().split())
print(eval(input()) == k)

Problem 41: Regex Split

regex_pattern = r"[,.]"
import re
print("\n".join(re.split(regex_pattern, input())))

Problem 42: String Sort

s = input()
print(''.join(sorted(s, key=lambda c: (c.isdigit() - c.islower(), c in '02468', c))))

Problem 43: Fibonacci Cubes

cube = lambda x: x**3

def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

print(list(map(cube, fibonacci(int(input())))))


Installation
To run the problems in this repository, you need to have Python installed. Follow these steps to set up your environment:

Clone the repository:

git clone https://github.com/Mamiololo01/Python-data_engineer_questions.git
cd Python-data_engineer_questions

Create a virtual environment:

python -m venv venv
source venv/bin/activate   # On Windows use `venv\Scripts\activate`

Install the required packages:

pip install -r requirements.txt

Usage

Each problem contains its own directory with specific instructions on how to run the examples. Refer to the README.md file within each directory for detailed usage instructions.

Contributing

We welcome contributions to this project. Please follow these steps to contribute:

Fork the repository:

Click the "Fork" button in the top-right corner of the repository page to create a copy of the repository in your GitHub account.
Clone the forked repository:


git clone https://github.com/your-username/Python-data_engineer_questions.git

cd Python-data_engineer_questions

Create a new branch:

git checkout -b my-feature

Make your changes:

Implement your changes or additions to the repository code. Ensure your code follows the existing 

Commit and push your changes:


git add .

git commit -m "Description of the changes"

git push origin my-feature

Create a pull request:

Go to your forked repository on GitHub and click on the "Compare & pull request" button to create a pull request to the original repository.

License

This project is licensed under the MIT License - see the LICENSE file for details.

Feel free to open an issue or contact the maintainers if you have any questions or need assistance.


