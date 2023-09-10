# Python-data_engineer_questions

Problem 2

If n is odd, print Weird
If n is even and in the inclusive range of 2 to 5, print Not Weird
If n is even and in the inclusive range of 6 to 20, print Weird
If n is even and greater than 20, print Not Weird
if n % 2 == 1:
    print("Weird")
elif n % 2 == 0 and n >= 2 and n <= 5:
    print("Not Weird")
elif n % 2 == 0 and n >= 6 and n <= 20:
    print("Weird")
elif n % 2 == 0 and n > 20:
    print("Not Weird")
    
Problem 3

The provided code stub reads two integers from STDIN, and . Add code to print three lines where:
The first line contains the sum of the two numbers.
The second line contains the difference of the two numbers (first - second).
The third line contains the product of the two numbers.
print(a+b)
print(a-b)
print(a*b)

Problem 4

The provided code stub reads two integers, a and b, from STDIN.
Add logic to print two lines.
The first line should contain the result of integer division, a // b.
The second line should contain the result of float division, a / b.
No rounding or formatting is necessary.
print(a//b)
print(a/b)

Problem 5

The provided code stub reads an integer, n, from STDIN.
For all non-negative integers i < n, print i^2.
for i in range (0,n):
    print(i**2)
    
Problem 6

An extra day is added to the calendar almost every four years as February 29,
and the day is called a leap day. It corrects the calendar for the fact that our planet
takes approximately 365.25 days to orbit the sun.
A leap year contains a leap day. In the Gregorian calendar, three conditions are used
to identify leap years:
The year can be evenly divided by 4, is a leap year, unless:
The year can be evenly divided by 100, it is NOT a leap year, unless
The year is also evenly divisible by 400. Then it is a leap year.
This means that in the Gregorian calendar, the years 2000 and 2400 are leap years,
while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.
def is_leap(year):
    leap = False
    # Write your logic here
    if(year % 400 == 0) :
        leap = True
    elif(year % 100 == 0) :
        leap = False
    elif(year % 4 == 0) :
        leap = True
    return leap
    
Problem 7

The included code stub will read an integer, n, from STDIN.
Without using any string methods, try to print the following:
123 ... n
Note that "..." represents the consecutive values in between.
for i in range (1, n+1):
print(i, end="")

Problem 8

Given the participants' score sheet for your University Sports Day,
you are required to find the runner-up score.
You are given scores. Store them in a list
and find the score of the runner-up.
The first line contains n. The second line contains an array A[] of integers n each separated by a space.
n = int(input())
arr = map(int, input().split())
arr = list(arr)
if len(arr) == 1:
    print(arr[0])
maximum = arr[0]
for i in range(0,n):
    if(arr[i] > maximum):
        maximum = arr[i]
secondHighest = -200
for j in range(0,n):
    if(arr[j] != maximum and arr[j] > secondHighest):
        secondHighest = arr[j]
print(secondHighest)

Problem 9

Given the names and grades for each student
in a class of N students, store them in a nested list
and print the name(s) of any student(s) having the second
lowest grade.

Note: If there are multiple students with the second
lowest grade, order their names alphabetically and
print each name on a new line.
listing = []
for _ in range(int(input())):
    name = input()
    score = float(input())
    listing_inner = []
    listing_inner.append(name)
    listing_inner.append(score)
    listing.append(listing_inner)
minimum = listing[0][1]
for grouping in listing:
    if grouping[1] < minimum:
        minimum = grouping[1]
secondLowestName = []
minimum2 = 120
for grouping in listing:
    if grouping[1] != minimum and grouping[1] < minimum2:
        minimum2 = grouping[1]
for grouping in listing:
    if grouping[1] == minimum2:
        secondLowestName.append(grouping[0])
secondLowestName.sort()
for name in secondLowestName:
    print(name)
    
Problem 10

The provided code stub will read in a dictionary containing key/value pairs of name:[marks]
for a list of students. Print the average of the marks array for the student name provided
, showing 2 places after the decimal.
scoresList = student_marks[query_name]
sum = 0
for mark in scoresList:
    sum += mark
print("{:.2f}".format(sum / len(scoresList)))
Problem 11
Consider a list (list = []). You can perform the following commands:
insert i e: Insert integer e at position i.
print: Print the list.
remove e: Delete the first occurrence of integer e.
append e: Insert integer e at the end of the list.
sort: Sort the list.
pop: Pop the last element from the list.
reverse: Reverse the list.
Initialize your list and read in the value of followed by lines
of commands where each command will be of the types listed above.
Iterate through each command in order and perform the corresponding operation
on your list.
result = []
for i in range (0,N):
    line = str(input())
    listy = line.split()
    command = listy[0]
    if command == "insert":
        argument1 = int(listy[1])
        argument2 = int(listy[2])
        result.insert(argument1, argument2)
    if command == "append":
        argument1 = int(listy[1])
        result.append(argument1)
    if command == "remove":
        argument1 = int(listy[1])
        result.remove(argument1)
    if command == "print":
        print(result)
    if command == "sort":
        result.sort()
    if command == "pop":
        result.pop()
    if command == "reverse":
        result.reverse()
        
Problem 12

Given an integer, n, and n space-separated integers as input,
create a tuple, t, of those n integers.
Then compute and print the result of hash(t).
tupling = tuple(integer_list)
print(hash(tupling))

Problem 13

You are given a string and your task is to swap cases.
In other words, convert all lowercase letters
to uppercase letters and vice versa.
def swap_case(s):
result = ""
for ch in s:
    if ch.isupper():
        result += ch.lower()
    elif ch.islower():
        result += ch.upper()
    else:
        result += ch
return result

Problem 14

You are given a string.
Split the string on a " " (space) delimiter
and join using a - hyphen.
def split_and_join(line):
    # write your code here
    split_words = line.split()
    result = ("-").join(split_words)
    return result
    
Problem 15

You are given the firstname and lastname of a person on two different lines.
Your task is to read them and print the following:
Hello firstname lastname! You just delved into python.
def print_full_name(a, b):
    print("Hello " + a + " " + b + "! You just delved into python.")
    
Problem 16

Read a given string, change the character at a given index
and then print the modified string.
def mutate_string(string, position, character):
    string_list = list(string)
    string_list[position] = character
    result = ("").join(string_list)
    return result
    
Problem 17

In this challenge, the user enters a string and a substring.
You have to print the number of times that the substring occurs in the given string.
String traversal will take place from left to right, not from right to left.
def count_substring(string, sub_string):
    count = 0
    for i in range (0, len(string)):
        if string[i:i+len(sub_string)] == sub_string:
            count = count + 1
    return count
    
Problem 18

You are given a string s.
Your task is to find out if the string contains:
alphanumeric characters, alphabetical characters, digits,
lowercase and uppercase characters.
s = input()
listy = list(s)
listBoolean = {"isalnum": False, "isalpha": False, "isdigit": False,
"islower": False, "isupper": False}
for i in range (0, len(listy)):
    if listy[i].isalnum():
        listBoolean["isalnum"] = True
    if listy[i].isalpha():
        listBoolean["isalpha"] = True
    if listy[i].isdigit():
        listBoolean["isdigit"] = True
    if listy[i].islower():
        listBoolean["islower"] = True
    if listy[i].isupper():
        listBoolean["isupper"] = True
print(listBoolean["isalnum"])
print(listBoolean["isalpha"])
print(listBoolean["isdigit"])
print(listBoolean["islower"])
print(listBoolean["isupper"])

Problem 19

You are given a string s and width w.
Your task is to wrap the string into a paragraph of width w.
def wrap(string, max_width):
    whole_string = list(string)
    new_list = []
    i = 0
    while i < len(string):
        for j in range(i,i+max_width):
            if j < len(whole_string):
                new_list.append(whole_string[j])
        new_list.append("\n")
        i = i + max_width
    return ("").join(new_list)
    
Problem 20

Mr. Vincent works in a door mat manufacturing company.
One day, he designed a new door mat with the following specifications:
Mat size must be N X M. (N is an odd natural number, and M is 3 times N.)
The design should have 'WELCOME' written in the center.
The design pattern should only use |, . and - characters.
dimensions = input()
height,width = dimensions.split()
height = (int)(height)
width = (int)(width)
stringPattern = ".|."
stringMultiple = ""
multiple = 0
for row in range(0, height//2):
    multiple = 1+2*row
    stringMultiple = stringPattern*multiple
    print(stringMultiple.center(width,"-"))
print("WELCOME".center(width,"-"))
for row in range((height//2)-1,-1,-1):
    multiple = 1+2*row
    stringMultiple = stringPattern*multiple
    print(stringMultiple.center(width,"-"))
    
Problem 21

Given an integer, n, print the following values
for each integer i from 1 to n:
Decimal
Octal
Hexadecimal (capitalized)
Binary

The four values must be printed on a single line
in the order specified above for each i from 1 to n.
Each value should be space-padded to match the width of the binary value of n.
def print_formatted(number):
    # your code goes here
    formatted_string = ""
    binary_length = 0
    for i in range(1, number+1):
        if(binary_length < len(bin(i)[2:])):
            binary_length = len(bin(i)[2:])
    for i in range(1,number+1):
        print (str(i).rjust(binary_length, " ")
+ " " + oct(i)[2:].rjust(binary_length, " ")
+ " " + str(hex(i)[2:].rjust(binary_length, " ")).upper()
+ " " + bin(i)[2:].rjust(binary_length, " "))
    return
  
Problem 22

You are given an integer, N.
Your task is to print an alphabet rangoli of size N.
(Rangoli is a form of Indian folk art based on creation of patterns.)
def print_rangoli(size):
    # your code goes here
    for row in range(0, size):
        letterInMiddle = chr(ord("a")+size-row-1)
        for j in range(row, 0, -1):
            letterInMiddle = chr(ord("a")+size-j) + "-" + letterInMiddle + "-" + chr(ord("a")+size-j)
        total_line = letterInMiddle.center((size*2-1)+(size*2-2),"-")
        print(total_line)
    for row in range(size-2, -1, -1):
        letterInMiddle = chr(ord("a")+size-row-1)
        for j in range(row, 0, -1):
            letterInMiddle = chr(ord("a")+size-j) + "-" + letterInMiddle + "-" + chr(ord("a")+size-j)
        total_line = letterInMiddle.center((size*2-1)+(size*2-2),"-")
        print(total_line)
    return total_line
    
Problem 23

You are asked to ensure that the first and last names of people
begin with a capital letter in their passports.
For example, alison heck should be capitalised correctly as Alison Heck.
# Complete the solve function below.
def solve(s):
    char_list = list(s)
    for ptr in range(0, len(char_list)):
        if char_list[ptr] == " " and char_list[ptr+1].isalpha():
            char_list[ptr+1] = char_list[ptr+1].upper()
        elif ptr == 0 and char_list[ptr].isalpha():
            char_list[ptr] = char_list[ptr].upper()
    result = ("").join(char_list)
    return result
    
Problem 24

Raghu is a shoe shop owner.
His shop has X number of shoes.
He has a list containing the size of each shoe he has in his shop.
There are N number of customers who are willing to pay x(i)
amount of money only if they get the shoe of their desired size.

Your task is to compute how much money Raghu earned.
from collections import Counter
number_of_shoes = int(input())
sizes_list = input().split()
counter_dt = Counter(sizes_list)
N = int(input())
total_sum = 0
for i in range(0,N):
    customer_demand = input().split()
    if customer_demand[0] in counter_dt.keys() and counter_dt[customer_demand[0]] > 0:
        total_sum = total_sum + int(customer_demand[1])
        counter_dt[customer_demand[0]] = counter_dt[customer_demand[0]] - 1
print(total_sum)

Problem 25

You are given a complex z.
Your task is to convert it to polar coordinates.
from cmath import phase
complex_coords = input()
complex_coords_1 = list()
if "+" in complex_coords:
    complex_coords_1 = complex_coords.split("+")
    complex_coords_1[1] = int(complex_coords_1[1][0:len(complex_coords_1[1])-1])
elif "-" in complex_coords[1:]:
    complex_coords_1.append(complex_coords[0:complex_coords[1:].index("-")+1])
    complex_coords_1.append(complex_coords[complex_coords[1:].index("-")+1:])
    complex_coords_1[1] = int(complex_coords_1[1][0:len(complex_coords_1[1])-1])
complex_coords_1[0] = int(complex_coords_1[0])
complex_coords_1[1] = int(complex_coords_1[1])
print(abs(complex(complex_coords_1[0], complex_coords_1[1])))
print(phase(complex(complex_coords_1[0], complex_coords_1[1])))

Problem 31

Ms. Gabriel Williams is a botany professor at District College.
One day, she asked her student Mickey to compute the average
of all the plants with distinct heights in her greenhouse.
The first line contains the integer, N, the total number of plants.
The second line contains the N space separated heights of the plants.
def average(array):
    # your code goes here
    set_array = set(array)
    sum = 0
    for val in set_array:
        sum += val
    average = sum / len(set_array)
    return average
    
Problem 32

You are the manager of a supermarket.You have a list of items together with their pricesthat consumers bought on a particular day.
Your task is to print each item_name and net_price in order of its first occurrence. from collections import OrderedDict
orderedDictionary = OrderedDict()
items_number = int(input())
for i in range(0, items_number):
    item_price_grouping = input().split(" ")
    price = int(item_price_grouping[len(item_price_grouping)-1])
    item_price_grouping.pop()
    item_name = (" ").join(item_price_grouping)
    if item_name not in orderedDictionary:
        orderedDictionary[item_name] = price
    else:
        orderedDictionary[item_name] = price + orderedDictionary.get(item_name)
for item_tuple in orderedDictionary:
    print(item_tuple + " " + str(orderedDictionary.get(item_tuple)))
    
Problem 33

You are given two values a and b.
Perform integer division and print a/b.
If there is division by 0 or value error print it out
lines = input()
for i in range(0,int(lines)):
    operate = input().split()
    try:
        print(int(int(operate[0]) / int(operate[1])))
    except ZeroDivisionError as e:
        print("Error Code: integer division or modulo by zero")
    except ValueError as e:
        print("Error Code: " + str(e))
        
Problem 34

You are given a date.
Your task is to find what the day is on that date.
import calendar
days = {0: "Monday", 1:"Tuesday", 2:"Wednesday", 3:"Thursday",
4:"Friday", 5:"Saturday", 6:"Sunday"}
date_list = input().split()
month = int(date_list[0])
date = int(date_list[1])
year = int(date_list[2])
day = calendar.weekday(year,month,date)
print(days[day].upper())

Problem 35

In this challenge, you will be given 2 integers, n and m.
There are n words, which might repeat, in word group A.
There are m words belonging to word group B.
For each m words, check whether the word has appeared in group A or not.
Print the indices of each occurrence of m in group A.
If it does not appear, print -1.
n,m = input().split()
n = int(n)
m = int(m)
from collections import defaultdict
d = defaultdict(list)
for i in range(0, n):
    word = input()
    d[word].append(i+1)
for i in range(0, m):
    word = input()
    if word in d.keys():
        for number in d[word]:
            print(number, end=" ")
    else:
        print(-1, end=" ")
    print()
    
Problem 36

The first line contains T, the number of testcases.
Each testcase contains 2 lines, representing time t1 and time t2.
Print the absolute difference (t1-t2) in seconds.
def time_delta(t1, t2):
    timeDelta = 3600*int(t1.split()[5][1:3])+ 60*int(t1.split()[5][3:])
    sign = t1.split()[5][0]
    hours = int(t1.split()[4].split(":")[0])
    minutes = int(t1.split()[4].split(":")[1])
    seconds = int(t1.split()[4].split(":")[2])
    months = {"Jan":1, "Feb":2, "Mar":3, "Apr":4, "May":5,
"Jun":6, "Jul":7, "Aug":8, "Sep":9, "Oct":10, "Nov":11, "Dec":12}
    year = int(t1.split()[3])
    month = int(months[t1.split()[2]])
    date = int(t1.split()[1])
    dt = datetime.datetime(year, month, date, hours, minutes, seconds)
    timestamp = dt.timestamp()
    if sign == "+":
        timestamp = timestamp - timeDelta
    else:
        timestamp = timestamp + timeDelta
    sign1 = t2.split()[5][0]
    timeDelta1 = 3600*int(t2.split()[5][1:3])+ 60*int(t2.split()[5][3:])
    hours1 = int(t2.split()[4].split(":")[0])
    minutes1 = int(t2.split()[4].split(":")[1])
    seconds1 = int(t2.split()[4].split(":")[2])
    year1 = int(t2.split()[3])
    month1 = int(months[t2.split()[2]])
    date1 = int(t2.split()[1])
    dt1 = datetime.datetime(year1, month1, date1, hours1, minutes1, seconds1)
    timestamp1 = dt1.timestamp()
    if sign1 == "+":
        timestamp1 = timestamp1 - timeDelta1
    else:
        timestamp1 = timestamp1 + timeDelta1
    return str(abs(int(timestamp1-timestamp)))
    
Problem 37
The students of District College have subscriptions to English and French newspapers.
Some students have subscribed only to English, some have subscribed only to French,
and some have subscribed to both newspapers.

You are given two sets of student roll numbers.
One set has subscribed to the English newspaper, one set has subscribed to the French newspaper.
Your task is to find the total number of students who have subscribed to both newspapers.
English_number = int(input())
English_roll = set(input().split())
French_number = int(input())
French_roll = set(input().split())
print(len(English_roll.intersection(French_roll)))

Problem 38

Students of District College have a subscription to English and French newspapers.
Some students have subscribed to only the English newspaper, some have subscribed to only the French newspaper,
and some have subscribed to both newspapers.
You are given two sets of student roll numbers.
One set has subscribed to the English newspaper, and one set has subscribed to the French newspaper.
Your task is to find the total number of students who have subscribed to only English newspapers.
English_number = int(input())
English_roll = set(input().split())
French_number = int(input())
French_roll = set(input().split())
print(len(English_roll.difference(French_roll)))

Problem 39

The students of District College have subscriptions to English and French newspapers.
Some students have subscribed only to English, some have subscribed to only French and some have subscribed to both newspapers.

You are given two sets of student roll numbers.
One set has subscribed to the English newspaper, and the other set is subscribed to the French newspaper.
The same student could be in both sets.
Your task is to find the total number of students who have subscribed to at least one newspaper.
English_count = int(input())
roll_numbers_english = set(input().split())
French_count = int(input())
roll_numbers_french = set(input().split())
print(len(roll_numbers_english.union(roll_numbers_french)))

Problem 40

Perform append, pop, popleft and appendleft methods on an empty deque d.
from collections import deque
operations_count = int(input())
d = deque()
for operation in range(0, operations_count):
    command_line = input().split()
    listy = command_line[1:]
    d1 = deque()
    for number in listy:
        d1.append(int(number))
    if command_line[0] == "append":
        d.append(listy)
    elif command_line[0] == "appendleft":
        d.appendleft(listy)
    elif command_line[0] == "pop":
        d.pop()
    elif command_line[0] == "popleft":
        d.popleft()
    elif command_line[0] == "extend":
        d.extend(listy)
    elif command_line[0] == "extendleft":
        d.extendleft(listy)
    elif command_line[0] == "remove":
        d.remove(listy)
    elif command_line[0] == "count":
        d.count(listy)
    elif command_line[0] == "reverse":
        d.reverse()
    elif command_line[0] == "rotate":
        d.rotate(listy)
for item in d:
    for i in item:
        print(i, end=" ")
        
Problem 41

Output 2 lines.
On the first line, output the number of distinct words from the input.
On the second line, output the number of occurrences for each distinct word
according to their appearance in the input.
number = input()
dt = {}
order_dt = {}
setty = set()
arrangements = set()
for i in range(0, int(number)):
    word = input()
    if word not in arrangements:
        order_dt[i] = word
        dt[word] = 1
        setty.add(i)
        arrangements.add(word)
    else:
        dt[word] = dt.get(word) + 1
print(len(dt))
for pt in range(0, int(number)):
    if pt in setty:
        print(dt[order_dt[pt]], end=" ")
        
Problem 42

You are given a string S.
Suppose a character 'c' occurs consecutively X times in the string.
Replace these consecutive occurrences of the character 'c'
with (X,c) in the string.
s = input()
current_ch = s[0]
count = 0
final_string = ""
ptr = 0
for ch in s:
    if ch != current_ch:
        stringy = "(" + str(count) + ", " + current_ch + ") "
        final_string = final_string + stringy
        current_ch = ch
        count = 1
        if ptr == len(s)-1:
            stringy = "(" + str(count) + ", " + current_ch + ") "
            final_string = final_string + stringy
    else:
        if ptr == len(s)-1:
            count = count + 1
            stringy = "(" + str(count) + ", " + current_ch + ") "
            final_string = final_string + stringy
        count = count + 1
    ptr = ptr + 1
print(final_string)

Problem 43

Mr. Anant Asankhya is the manager at the INFINITE hotel.
The hotel has an infinite amount of rooms.

One fine day, a finite number of tourists come to stay at the hotel.
The tourists consist of:
→ A Captain.
→ An unknown group of families consisting of K members per group where K ≠ 1.

The Captain was given a separate room,
and the rest were given one room per group.

Mr. Anant has an unordered list of randomly arranged room entries.
The list consists of the room numbers for all of the tourists.
The room numbers will appear K times per group except for the Captain's room.

Mr. Anant needs you to help him find the Captain's room number.
The total number of tourists or the total number
of groups of families is not known to you.
You only know the value of K and the room number list.
K = int(input())
listy = input().split()
bunch = len(listy)-1 // K
setty = set()
discarded = set()
for i in range(0, len(listy)):
    if listy[i] not in setty:
        setty.add(listy[i])
    else:
        discarded.add(listy[i])
for num in setty.difference(discarded):
    print(num)
    
Problem 44

There is an array of n integers.
There are also 2 disjoint sets,
A and B, each containing m integers.
You like all the integers in set A
and dislike all the integers in set B.
Your initial happiness is 0.
For each integer in the array,
if i belongs to A, you add 1 to your happiness.
If i belongs to B, you add -1 to your happiness.
Otherwise, your happiness does not change.
Output your final happiness at the end.

Note: Since A and B are sets, they have no repeated elements.
However, the array might contain duplicate elements.
first_line = input()
provided_numbers_length = int(first_line.split()[0])
A_B_length = int(first_line.split()[1])
provided_numbers = input().split()
A = input().split()
B = input().split()
setty = set()
setty1 = set()
for number in A:
    setty.add(number)
for number in B:
    setty1.add(number)
happiness = 0;
for number in provided_numbers:
    if number in setty:
        happiness = happiness + 1
    elif number in setty1:
        happiness = happiness - 1
print(happiness)

Problem 45

There is a horizontal row of n cubes.
The length of each cube is given.
You need to create a new vertical pile of cubes.
The new pile should follow these directions:
if cube(i) is on top of cube(j)
then sideLength(j) > sideLength(i).

When stacking the cubes, you can only
pick up either the leftmost or the
rightmost cube each time.
Print "Yes" if it is possible to stack the cubes.
Otherwise, print "No".
Do not print the quotation marks.
from collections import deque
d = deque()
l = list()
cases = int(input())
escape = False
for i in range(0, cases):
    d.clear()
    cubes_number = int(input())
    cubes = input().split()
    for cube in cubes:
        d.append(int(cube))
    while len(d) > 0:
        if int(d[len(d)-1]) > int(d[0]):
            if len(l) > 0 and int(d[len(d)-1]) > l[len(l)-1]:
                print("No")
                escape = True
                break
            l.append(int(d[len(d)-1]))
            d.pop()
        else:
            if len(l) > 0 and int(d[0]) > l[len(l)-1]:
                print("No")
                escape = True
                break
            l.append(int(d[0]))
            d.popleft()
    l.clear()
    if escape == True:
        escape = False
        continue
    print("Yes")
    
Problem 46

This tool returns the r length subsequences
of elements from the input iterable.

Combinations are emitted in lexicographic sorted order.
So, if the input iterable is sorted,
the combination tuples will be produced in sorted order.
given = input().split()
word = given[0]
sorted1 = list(word)
sorted1.sort()
word_final = "".join(sorted1)
k = int(given[1])
from itertools import combinations
for i in range(1, k+1):
    listy = list(combinations(word_final, i))
    for w in listy:
        for ptr in w:
            print(ptr, end="")
        print()
        
Problem 47

You are given two sets, A and B.
Your job is to find whether set A is a subset of set B.

If set A is subset of set B, print True.
If set A is not a subset of set B, print False.
cases = int(input())
for i in range(0, cases):
    A_length = int(input())
    A = input().split()
    B_length = (int((input())
    B = (input().split()
    if A_length > B_length:
        print(False)
        continue
    subset = True
    for item_A in A:
        if item_A not in B:
            subset = False
    print(subset)
    
Problem 48

You are given a set A and n other sets.
Your job is to find whether set A is a strict superset of each of the n sets.

Print True, if A is a strict superset of each of the n sets.
Otherwise, print False.

A strict superset has at least one element that
does not exist in its subset.
A = set(input().split())
sets = int(input())
strict_superset = True
completed = False
for i in range(0, sets):
    set_temp = set(input().split())
    ptr = 0
    for item_temp in set_temp:
        if item_temp not in A:
            strict_superset = False
            print(strict_superset)
            break
        elif item_temp in A and len(A) > len(set_temp) and ptr == len(set_temp) - 1 and i == sets - 1:
            print(strict_superset)
            completed = True
            break
        ptr = ptr + 1
    if strict_superset == False:
        break
    elif completed == True:
        break
        
Problem 49

You are given a polynomial P of a single indeterminate (or variable), x.
You are also given the values of x and k.
Your task is to verify if P(x) = k.
inputs = input().split()
x = int(inputs[0])
k = int(inputs[1])
statement = input()
statement = statement.replace("x", str(x))
print(eval(statement) == k)
Problem 50
The first line contains N and X separated by a space.
The next X lines contains the space separated marks obtained by students in a particular subject.

Print the averages of all students on separate lines.

The averages must be correct up to decimal place.
cases = input().split()
cases[1] = int(cases[1])
marks = list()
for c in range(0,cases[1]):
    marks.append(input().split())
final_list = list()
for m in range (0,len(marks)):
    if m == 0:
        final_list = [marks[m]]
    else:
        final_list = final_list + [marks[m]]
final_list_1 = zip(*final_list)
sum = 0
for lis in final_list_1:
    for num in lis:
        sum = sum + float(num)
    print(sum / len(lis))
    sum = 0
Problem 51
You are given a string s consisting
only of digits 0-9, commas ,, and dots .

Your task is to complete the regex_pattern defined below
, which will be used to re.split() all of the , and . symbols in s.
regex_pattern = r",|\."
import re
print("\n".join(re.split(regex_pattern, input())))

Problem 52

You are given an expression in a line.
Read that line as a string variable, such as var,
and print the result using eval(var).
command = input()
eval(command)
Problem 53
You are given a string S.
S contains alphanumeric characters only.
Your task is to sort the string S in the following manner:
All sorted lowercase letters are ahead of uppercase letters.
All sorted uppercase letters are ahead of digits.
All sorted odd digits are ahead of sorted even digits.
stringy = input()
stringy_lower = ""
stringy_upper = ""
digits_list = []
for ptr in range(0,len(stringy)):
    if stringy[ptr].isalpha() and stringy[ptr].isupper():
        stringy_upper = stringy_upper + stringy[ptr]
    elif stringy[ptr].isalpha() and stringy[ptr].islower():
        stringy_lower = stringy_lower + stringy[ptr]
    elif stringy[ptr].isdigit():
        digits_list.append(int(stringy[ptr]))
digits_list.sort()
stringy_lower_sorted = ""
minimum = ord("z")
ch = ""
done_chars_ptr = set()
ptr_final = 0
while len(stringy_lower_sorted) < len(stringy_lower):
    for ptr in range(0,len(stringy_lower)):
        if minimum >= ord(stringy_lower[ptr]) and ptr not in done_chars_ptr:
            minimum = ord(stringy_lower[ptr])
            ch = stringy_lower[ptr]
            ptr_final = ptr
    done_chars_ptr.add(ptr_final)
    stringy_lower_sorted = stringy_lower_sorted + ch
    minimum = ord("z")
stringy_upper_sorted = ""
minimum = ord("Z")
ch = ""
done_chars_ptr = set()
ptr_final = 0
while len(stringy_upper_sorted) < len(stringy_upper):
    for ptr in range(0,len(stringy_upper)):
        if minimum >= ord(stringy_upper[ptr]) and ptr not in done_chars_ptr:
            minimum = ord(stringy_upper[ptr])
            ch = stringy_upper[ptr]
            ptr_final = ptr
    done_chars_ptr.add(ptr_final)
    stringy_upper_sorted = stringy_upper_sorted + ch
    minimum = ord("Z")
alphabets_sorted = stringy_lower_sorted + stringy_upper_sorted
numbers_string = ""
for digi in digits_list:
    if digi % 2 != 0:
        numbers_string = numbers_string + str(digi)
for digi in digits_list:
    if digi % 2 == 0:
        numbers_string = numbers_string + str(digi)
print(alphabets_sorted + numbers_string)

Problem 54

A list on a single line containing the cubes of the first
fibonacci numbers.

cube = lambda x: x**3
def fibonacci(n):
    listy = []
    num = 0
    while num < n:
        if num == 0 or num == 1:
            listy.append(num)
        else:
            answer = listy[num-2] + listy[num-1]
            listy.append(answer)
        num = num + 1
    return listy
    
Problem 55

You are given a string N.
Your task is to verify that N is a floating point number.

import re
cases = int(input())
for i in range(0, cases):
    string = input()
    print(re.search("(^[+,\-,\.,]?(\d)+?(\.)?\d+$)|(^[+,\-,\.,]?(\d)?(\.)+\d+$)", string)!=None)
    
Problem 56

You are given a spreadsheet that contains a list of
N athletes and their details (such as age, height, weight and so on).
You are required to sort the data based on the Nth attribute
and print the final resulting table.
Follow the example given below for better understanding.

list_arranged = []
temp = 0
temp_arr = []
found_row = 0
while len(arr) > 0:
    ptr = 0
    for row in arr:
        if ptr == 0:
            minimum = row[k]
            temp = row
            found_row = ptr
        if minimum > row[k]:
            minimum = row[k]
            temp = row
            found_row = ptr
        ptr = ptr + 1
    list_arranged.append(temp)
    temp_arr.clear()
    for i in range(0, len(arr)):
        if i != found_row:
            temp_arr.append(arr[i])
    arr = temp_arr.copy()
for result in list_arranged:
    for num in result:
        print(num, end=" ")
    print()
    
Problem 57

It's New Year's Day and everyone's in line for the Wonderland rollercoaster ride!
There are a number of people queued up,
and each person wears a sticker indicating their initial position in the queue.
Initial positions increment by 1 from 1 at the front of the line to n at the back.

Any person in the queue can bribe the person directly in front of them to swap positions.
If two people swap positions,
they still wear the same sticker denoting their original places in line.
One person can bribe at most two others.

def minimumBribes(q):
    count = 0
    doneNums = dict()
    ptr = len(q)-1
    position = len(q)-1
    while ptr > -1:
        if q[ptr] != ptr + 1 and q[ptr] > q[ptr-1] and ptr >= q[ptr] - 3 and (q[ptr-1] not in doneNums
or (q[ptr-1] in doneNums and doneNums.get(q[ptr-1]) < 3)):
            position = ptr
        elif q[ptr] != ptr + 1 and q[ptr] < q[ptr-1] and ptr >= q[ptr] - 3 and (q[ptr-1] not in doneNums
or (q[ptr-1] in doneNums and doneNums.get(q[ptr-1]) < 3)):
            if q[ptr-1] not in doneNums:
                doneNums[q[ptr-1]] = 1
            if q[ptr-1] in doneNums:
                doneNums[q[ptr-1]] = doneNums.get(q[ptr-1]) + 1
            temp = q[ptr]
            q[ptr] = q[ptr-1]
            q[ptr-1] = temp
            count = count + 1
            ptr = position + 1
        elif q[ptr] != ptr + 1 and (q[ptr-1] in doneNums and doneNums.get(q[ptr-1]) >= 2):
            print("Too chaotic")
            return
        ptr = ptr - 1
    for ptr in range(len(q)-1,-1,-1):
        if ptr-1 >= 0 and q[ptr] < q[ptr-1]:
            print("Too chaotic")
            return
    print(count)
    
Problem 58

You are given an unordered array consisting of consecutive integers [1, 2, 3, ..., n]
without any duplicates.
You are allowed to swap any two elements.
You need to find the minimum number of swaps required to sort the array in ascending order.

def minimumSwaps(arr):
    count = 0
    ptr = 0
    while ptr < len(arr):
        if arr[ptr] != ptr + 1:
            temp = arr[ptr]
            temp2 = arr[ptr]-1
            arr[ptr] = arr[temp2]
            arr[temp2] = temp
            count = count + 1
        else:
            ptr = ptr + 1
    return count
Problem 59
Sherlock considers a string to be valid if all characters of the string appear the same number of times.
It is also valid if he can remove just 1 character at 1 index in the string,
and the remaining characters will occur the same number of times.
Given a string , determine if it is valid. If so, return YES, otherwise return NO.

def isValid(s):
    dt = dict()
    for ch in s:
        if ch in dt:
            dt[ch] = dt.get(ch) + 1
        else:
            dt[ch] = 1
    print(dt)
    dt2 = dict()
    for value in dt.values():
        if value in dt2:
            dt2[value] = dt2.get(value) + 1
        else:
            dt2[value] = 1
    print(dt2)
    if len(dt2) == 1:
        return("YES")
    elif len(dt2) == 2:
        moreThanOne = -1
        for item in dt2:
            if item > 1 and moreThanOne == -1:
                moreThanOne = item
            elif dt2[item] > 1 and moreThanOne != -1:
                return("NO")
        return("YES")
    else:
        return("NO")
        
Problem 60

Each time Sunny and Johnny take a trip to the Ice Cream Parlor,
they pool their money to buy ice cream.
On any given day, the parlor offers a line of flavors.
Each flavor has a cost associated with it.

Given the value of and the of each flavor for trips to the Ice Cream Parlor,
help Sunny and Johnny choose two distinct flavors
such that they spend their entire pool of money during each visit.
ID numbers are the 1- based index number associated with a .
For each trip to the parlor, print the ID numbers for the two types of ice cream
that Sunny and Johnny purchase as two space-separated integers on a new line.
You must print the smaller ID first and the larger ID second.

def whatFlavors(cost, money):
    dt = dict()
    for ptr in range (0, len(cost)):
        if ptr not in dt:
            dt[cost[ptr]] = [ptr]
        else:
            dt[cost[ptr]] = dt.get(ptr) + [ptr]
    for ptr in range(0, len(cost)):
        if (money - cost[ptr]) in dt and ptr != dt[money-cost[ptr]][len(dt[money-cost[ptr]])-1]:
            print(ptr+1, dt[money-cost[ptr]][len(dt[money-cost[ptr]])-1]+1)
            break

Problem 61

You will be given an array of integers and a target value.
Determine the number of pairs of array elements that have a difference equal to a target value.

def pairs(k, arr):
    ptr = 0
    dt = dict()
    while ptr < len(arr):
        if arr[ptr] not in dt:
            dt[arr[ptr]] = 1
        elif arr[ptr] in dt:
            dt[arr[ptr]] = dt.get(arr[ptr]) + 1
        ptr = ptr + 1
    count = 0
    for ptr in range(0,len(arr)):
        if arr[ptr] - k in dt:
            count = count + 1
    return(count)

Problem 62

You are given a string containing characters A and B only.
Your task is to change it into a string such that there are
no matching adjacent characters.
To do this, you are allowed to delete
zero or more characters in the string.

Your task is to find the minimum number of required deletions.

def alternatingCharacters(s):
    ch = s[0]
    deletions = 0
    for ptr in range(1, len(s)):
        if ch != s[ptr]:
            ch = s[ptr]
            continue
        else:
            deletions = deletions + 1
    return deletions

Problem 63

Complete the makeAnagram function in the editor below.
It must return an integer representing the minimum total characters
that must be deleted to make the strings anagrams.

def makeAnagram(a, b):
    setA = set()
    setB = set()
    dtA = dict()
    dtB = dict()
    for ch in a:
        setA.add(ch)
        if ch not in dtA:
            dtA[ch] = 1
        else:
            dtA[ch] = dtA.get(ch) + 1
    for ch in b:
        setB.add(ch)
        if ch not in dtB:
            dtB[ch] = 1
        else:
            dtB[ch] = dtB.get(ch) + 1
    setC = setA.difference(setB).union(setB.difference(setA))
    count = 0
    for ch in setC:
        if ch in dtA:
            count = count + dtA[ch]
        else:
            count = count + dtB[ch]
    for ch in dtA:
        if ch not in setC and dtA[ch] != dtB[ch]:
            count = count + abs(dtA[ch] - dtB[ch])
    return count

Problem 64

Complete the checkMagazine function in the editor below.
It must print Yes if the note can be formed using the magazine, or No.
checkMagazine has the following parameters:
magazine: an array of strings, each a word in the magazine
note: an array of strings, each a word in the ransom note

def checkMagazine(magazine, note):
    dt = dict()
    dt1 = dict()
    for word in magazine:
        if word not in dt:
            dt[word] = 1
        else:
            dt[word] = dt.get(word) + 1
    for word in note:
        if word not in dt1:
            dt1[word] = 1
        else:
            dt1[word] = dt1.get(word) + 1
    for word in dt1:
        if word not in dt or dt1[word] > dt[word]:
            print("No")
            return
    print("Yes")

Problem 65

Complete the function twoStrings in the editor below.
It should return a string, either YES or NO
based on whether the strings share a common substring.

twoStrings has the following parameter(s):
s1, s2: two strings to analyze .

def twoStrings(s1, s2):
    set1 = set()
    set2 = set()
    for ch in s1:
        set1.add(ch)
    for ch in s2:
        set2.add(ch)
    if len(set1.intersection(s2)) > 0:
        return("YES")
    else:
        return("NO")
