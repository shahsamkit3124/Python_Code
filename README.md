# Python_Code

# 1 Write a Python program to draw a scatter plot with empty circles taking a random distribution in X and Y and plotted against each other.

import matplotlib.pyplot as plt 
import numpy as np 
import math
x = np.random.randn(50) 
y = np.random.randn(50)
plt.scatter(x, y, s=70, facecolors='none', edgecolors='g') # s is the size of circles 
plt.xlabel("X")
plt.ylabel("Y")
plt.show()

------------------------------------------------------------------------------------------------------------

# 2 Write a Python program to draw a scatter plot using random distributions to generate balls of different sizes.

import matplotlib.pyplot as plt 
import numpy as np 
import math
x = np.random.randn(50)
y = np.random.randn(50)
z = math.pi * np.random.randn(50)*3
plt.scatter(x,y,s=z,edgecolors='r')
plt.show()

------------------------------------------------------------------------------------------------------------

# 3 Write a Python program to draw a scatter plot comparing two subject marks of Mathematics and Science. Use marks of 10 students. Sample data:math_marks = [88, 92, 80, 89, 100, 80, 60, 100, 80, 34]science_marks = [35, 
# 79, 79, 48, 100, 88, 32, 45, 20, 30]marks_range= [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]

import matplotlib.pyplot as plt 
import numpy as np 
import math
math_marks = [88, 92, 80, 89, 100, 80, 60, 100, 80, 34]
science_marks = [35, 79, 79, 48, 100, 88, 32, 45, 20, 30]
marks_range = [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]
plt.scatter(marks_range, math_marks, label='Math marks', color='r')
plt.scatter(marks_range, science_marks, label='Science marks', color='g')
plt.title('Scatter Plot')
plt.xlabel('Marks Range')
plt.ylabel('Marks Scored')
plt.legend()
plt.show()

------------------------------------------------------------------------------------------------------------

# 4 Write a Python script to concatenate following dictionaries to create a new one.
# Sample Dictionary :
# dic1={1:10, 2:20}
# dic2={3:30, 4:40}
# dic3={5:50,6:60}
# Expected Result : {1: 10, 2: 20, 3: 30, 4: 40, 5: 50, 6: 60}

import random
import math
dic1={1:10, 2:20}
dic2={3:30, 4:40}
dic3={5:50,6:60}
dic4 = {**dic1, **dic2, **dic3}
print(dic4)

------------------------------------------------------------------------------------------------------------

# 5 Write a Python script to check whether a given key already exists in a dictionary.

import random
import math
i = 4
if i in dic4:
    print(i," is present")
else:
    print(i," is not present")

------------------------------------------------------------------------------------------------------------

# 6 Write a Python script to generate and print a dictionary that contains a number (between 1 and n) in the form (x, x*x).Sample Dictionary( n = 5) : Expected Output : {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

import random
import math
dic5 = {}
for i in range(1,6):
    dic5[i] = i*i
print(dic5)

------------------------------------------------------------------------------------------------------------

# 7 Write a Python program to remove a key from a dictionary

import random
import math
dic5 = {}
for i in range(1,6):
    dic5[i] = i*i
print(dic5)
dic5.pop(3)
print(dic5)

------------------------------------------------------------------------------------------------------------

# 8 Write a Python program to map two lists into a dictionary.

import random
import math
l1 = [1,2,3,4]
l2 = [5,6,7,8]
dic6 = dict(zip(l1,l2))
print(dic6)

------------------------------------------------------------------------------------------------------------

# 9 Write a Python program to print all unique values in a dictionary Sample Data : [{"V":"S001"}, {"V": "S002"}, {"VI": "S001"}, {"VI": "S005"}, {"VII":"S005"}, {"V":"S009"},{"VIII":"S007"}] Expected Output : Unique # # # # Values: {'S005', 'S002', 'S007', 'S001', 'S009'}

import random
import math
L = [{"V":"S001"}, {"V": "S002"}, {"VI": "S001"}, {"VI": "S005"}, {"VII":"S005"}, {"V":"S009"},{"VIII":"S007"}]
print("Original List: ",L)
s = set()
for dic in L:
    for val in dic.values():
        s.add(val)
print("Unique Values: ",s)

------------------------------------------------------------------------------------------------------------

# 10 Write a Python program to create a dictionary from a string. Note: Track the count of the letters from the string.

import random
import math
str1 = 'pythonprac' 
my_dict = {}
for letter in str1:
    my_dict[letter] = my_dict.get(letter, 0) + 1  #get use karne ne default value daal sakte hai , warna error aata
print(my_dict)

------------------------------------------------------------------------------------------------------------

# 11 Write a program that takes a sentence as an input parameter where each word in the sentence is separated by a space. Then replace each blank with a hyphen and then print the modified sentence.

import random
import math
string = input("Enter a sentence: ") 
newstr = string.replace(" ","-") 
print(newstr)

------------------------------------------------------------------------------------------------------------

# 12 Write a program to randomly select 10 integer elements from range 100 to 200 and find the smallest among all.

import random
import math
rno = min(random.sample(range(100, 200), 10))
print(rno)

-----------------------------------------------------------------------------------------------------------

# 13 Create a dictionary of 5 countries with their currency details and display them. 
# Print as below 
# First line
# Second line
# Third Line 

import random
import math
dict = {"Afghanistan":"Afghani","Luxembourg ":"Euro","Qatar":"Qatari Riyal","Vietnam":"Dong","India":"Rupee"}
for i,j in dict.items():
    print(i,":",j)

-----------------------------------------------------------------------------------------------------------

# 14 Declare complex number , find data type, real part, imaginary part, complex conjugate, absolute value of a number

import random
import math
comnum = 3+2j
comnum2 = complex(3,2)
print(type(comnum))
print(comnum.real)
print(comnum.imag)
print(comnum.conjugate())
def magnitude(comnum):
    r = comnum.real
    i = comnum.imag
    ans = r*r + i*i
    return math.sqrt(ans)
print(magnitude(comnum))

-----------------------------------------------------------------------------------------------------------

# 15 Change string hello to help  ,remove white spaces before word if  s=”   hello ” 

import random
import math
str = "   hello"
str = str.lstrip()
str = str.replace("llo","lp")
print(str)

-----------------------------------------------------------------------------------------------------------

# 17 Swap first & last letter of a string 

import random
import math
str = "firstandlast"
strnew = str[-1:] + str[1:-1] + str[:1]
print(strnew)

-----------------------------------------------------------------------------------------------------------

# 18 Find if substring is present in string or not

import random
import math
str = "ispresent"
if "present" in str:
    print("present is present")
else:
    print("present is not present")

-----------------------------------------------------------------------------------------------------------

# 20 WAPP to test whether string is palindrome or not 

import random
import math
str = "biggib"
revstr = reversed(str)
if list(str) == list(revstr):
    print(True)
else:
    print(False)

-----------------------------------------------------------------------------------------------------------

# 21 WAP to capitalize the first character of each words from a given sentence (example: all the best All The Best) 

import random
import math
str = "hello world"
str = str.title()
print(str)

-----------------------------------------------------------------------------------------------------------

# 22 WAP to count the frequency of occurrence of a given character in a given line of text 

import random
import math
str = "hello world"
map = {}
for i in str:
    map[i] = map.get(i,0) +1 
print(map)

-----------------------------------------------------------------------------------------------------------

# 23 Create a dictionary of 4 states with their capital details & add one more pair to the same

import random
import math
dict = {
    "state1":"cap1",
    "state2":"cap2",
    "state3":"cap3",
    "state4":"cap4",
}
dict["state5"] = "cap5"
print(dict)

-----------------------------------------------------------------------------------------------------------

# 24 To count number digits, special symbols from the given sentence. Also count number of vowels and consonants

import random
import math
def countCharacterType(str):
    vowels = 0
    consonant = 0
    specialChar = 0
    digit = 0
    for i in range(0, len(str)):
        ch = str[i]
        if ( (ch >= 'a' and ch <= 'z') or
             (ch >= 'A' and ch <= 'Z') ):
            ch = ch.lower()
            if (ch == 'a' or ch == 'e' or ch == 'i'
                        or ch == 'o' or ch == 'u'):
                vowels += 1
            else:
                consonant += 1
        elif (ch >= '0' and ch <= '9'):
            digit += 1
        else:
            specialChar += 1
    print("Vowels:", vowels)
    print("Consonant:", consonant)
    print("Digit:", digit)
    print("Special Character:", specialChar)
str = "Password23@#"
countCharacterType(str)

-----------------------------------------------------------------------------------------------------------

# 25 Write a program to accept any string up to 15 characters. Display the elements of string with their element nos

import random
import math
str = input("Enter a string with less then 15 letter: ")
if(len(str)>15):
    print("Enter a string with less characters")
else:
    for i in range(len(str)):
        print(i,":",str[i])

-----------------------------------------------------------------------------------------------------------

# 26 Create a Numpy array filled with all ones

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
arr = np.ones(5)
print(arr)

------------------------------------------------------------------------------------------------------------

# 27 Check whether a Numpy array contains a specified row

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
arr = np.array([[1, 2, 3, 4, 5],
                   [6, 7, 8, 9, 10],
                   [11, 12, 13, 14, 15],
                   [16, 17, 18, 19, 20]
                   ])
print(arr)
print([1, 2, 3, 4, 5] in arr.tolist())
print([16, 17, 20, 19, 18] in arr.tolist())

------------------------------------------------------------------------------------------------------------

# 28 Compute mathematical operations on Array, Add & Multiply two matrices

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
mat1 = ([1, 6, 5],[3 ,4, 8],[2, 12, 3])
mat2 = ([3, 4, 6],[5, 6, 7],[6,56, 7])
res = np.dot(mat1,mat2)
print(res)
res = np.add(mat1,mat2)
print(res)

------------------------------------------------------------------------------------------------------------

# 29 Find the most frequent value in a NumPy array 

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
arr = np.array([1,1,1,2,3,])
print(np.bincount(arr).argmax())

------------------------------------------------------------------------------------------------------------

# 30 Flatten a 2d numpy array into 1d array

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
arr = np.array([[1,2,3,4],[5,6,7,8]])
arr = arr.flatten()
print(arr)

------------------------------------------------------------------------------------------------------------

# 31 Calculate the sum of all columns in a 2D NumPy array

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
num = np.arange(36)
arr1 = np.reshape(num, [4, 9])
print("Original array:")
print(arr1)
result  = arr1.sum(axis=0)
print("\nSum of all columns:")
print(result)

------------------------------------------------------------------------------------------------------------

# 32 Calculate the average, variance and standard deviation in Python using NumPy

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
arr = np.array([1,2,3,4,5])
print(arr.mean())
print(arr.std())
print(arr.var())

------------------------------------------------------------------------------------------------------------

# 33 Insert a space between characters of all the elements of a given NumPy array ['Python' 'is' 'easy']  ['P y t h o n' 'i s' 'e a s y'] 

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
x = np.array(["Python","is","easy"])
print(x)
r = np.char.join(" ",x)
print(r)

------------------------------------------------------------------------------------------------------------

# 34 Plot line graph from NumPy array

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
x = np.array([1,2,3,4,5])
plt.plot(x,x)
plt.show()

------------------------------------------------------------------------------------------------------------

# 35 WAP to Reverse a Number  

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
num = 1345
revnum = 0
while num>0:
    temp = num%10
    revnum = revnum*10 + temp
    num //= 10
print(revnum)

------------------------------------------------------------------------------------------------------------

# 36 WAP to read number N and print natural numbers summation pattern

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
number = int(input("Enter the Natural Number: "))
for j in range(1, number+1):
    num = 0
    for i in range(1, j+1):
        print(i, sep=" ", end=" ")
        if(i < j):
            print("+", sep=" ", end=" ")
        num += i
    print("=", num)

------------------------------------------------------------------------------------------------------------

# 37 WAP to determine all Pythagorean triplets  

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
limit = 30
c = 0
m = 2
while c<limit:
    for n in range(1,m):
        a = m*m - n*n
        b = 2*m*n
        c = m*m + n*n
        if(c>limit):
            break
        print(a,b,c)
    m = m+1

------------------------------------------------------------------------------------------------------------

# 38 WAP, You are given a number A which contains only digits 0's and 1's. Your task is to make all digits same by just flipping one digit (i.e. 0 to 1 or 1 to 0 ) only. If it is possible to make all the digits same by just flipping one digit then print 'YES' else print 'NO'.

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
num = 101
str = str(num)
zeros = 0
ones = 0
for i in range (len(str)):
    if(str[i] == '0'):
        zeros += 1
    else:
        ones += 1
if(zeros == 1 or ones == 1):
    print("YES")
else:
    print("NO")

------------------------------------------------------------------------------------------------------------

# 39 Given a list A of N distinct integer numbers, you can sort the list by moving an element to the end of the list. Find the minimum number of moves required to sort the list using this method in ascending order   

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
l=list(map(int,input().split(" ")))
print(l)
c=0
y=0
while y < len(l)-1:
    min=l[y]
    val=l[y]
    for x in range(y+1, len(l)):
        val=l[x]
        if val < min:
            break
    if val < min:
        l.remove(min) 
        l.append(min)
        c=c+1
    else:
        y=y+1
print(c)

------------------------------------------------------------------------------------------------------------

# 40 WAP to print following pattern
# 1\n
# 22\n
# 333\n
# 4444\n
# 55555\n
# 666666

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
for i in range (1,7):
    for j in range(1,i+1):
        print(i,end = "")
    print("")

------------------------------------------------------------------------------------------------------------

# 41 Convert two lists into a dictionary

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
key = [1,2,3,4,5]
val = ['a','b','c','d','e']
dict = {}
for i in range(0,len(key)):
    dict[key[i]] = val[i]
print(dict)
res = dict(zip(key, val))
print(res)

------------------------------------------------------------------------------------------------------------

# 42 Check how many times a given number can be divided by 6 before it is less than or equal to 10.  

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
inp = int(input("Enter a number: "))
c= 0
while inp>=10:
    inp //= 6
    c+=1
print(c)

------------------------------------------------------------------------------------------------------------

# 43 Python program to read a file and Capitalize the first letter of every word in the file

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
with open("temp.txt",'r') as f:
    for line in f:
        print(line.title())
f.close

------------------------------------------------------------------------------------------------------------

# 44 Python program that reads a text file and counts number of times certain letter appears in the text file

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
with open("temp.txt",'r') as f:
    dict = {}
    for line in f:
        for letter in line:
            dict[letter] = dict.get(letter,0) +1
    print(dict)
f.close()

------------------------------------------------------------------------------------------------------------ 

# 45 Write a program to write content to file &  append data to file

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
# part 1
with open("temp.txt",'w') as f:
    f.write("HELLO WORLD")
    f.close()
with open("temp.txt",'r') as f:
    print(f.read())
# part 2
with open("temp.txt",'a') as f:
    f.write("HELLO WORLD")
    f.close()
with open("temp.txt",'r') as f:
    print(f.read())

------------------------------------------------------------------------------------------------------------ 

# 46 Python program to read the contents of a file  

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
with open('example.txt', 'r') as file:
    file_contents = file.read()
    print("File contents:")
    print(file_contents)

------------------------------------------------------------------------------------------------------------ 

# 47 Copy the contents from one file to another

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
f2 = open("temp2.txt",'a')
f = open("temp.txt",'r')
cont  = f.read()
f2.write(cont)

------------------------------------------------------------------------------------------------------------ 

# 48 WAP to accept name and roll number of students and store it in file. Read and display the stored data. Also check if file exists or not

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
f = open("temp2.txt",'a')
n = int(input("Enter the number of students: "))
for i in range(0,n):
    name = input("Enter the name of the student: ")
    roll = input("Enter the roll number of the student: ")
    str = name+":"+roll
    f.write(str)
    f.write("\n")
f.close()
path = "temp2.txt"
isExist = os.path.exists(path)
print(isExist)

------------------------------------------------------------------------------------------------------------ 

# 49 WAP to copy contents of 1 file to another Let user specify name of source and destination files 

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
file1 = input("Enter the first file :")
file2 = input("Enter the second file :")
f2 = open(file2,'a')
with open(file1,'r') as f:
    for line in f:
        f2.write(line)

------------------------------------------------------------------------------------------------------------ 

# 50 Python program to read file word by word  

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
f = open("temp.txt",'r')
for line in f:
    list = line.split(" ")
    for i in list:
        print(i)

------------------------------------------------------------------------------------------------------------ 

# 51 Python program to read character by character from a file

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
f = open("temp.txt",'r')
for line in f:
    for char in line:
        print(char)
        
------------------------------------------------------------------------------------------------------------ 

# 52 Python – Get number of characters, words, spaces and lines in a file

from itertools import count
import matplotlib.pyplot as plt
import numpy as np
import os.path
char = 0
word = 0
lines = 0
f = open("temp.txt",'r')
for line in f:
    lines  = lines + 1
    list = line.split(" ")
    word = word + len(list)
    for chars in line:
        char = char + 1
print(char)
print(word)
print(lines)
        
------------------------------------------------------------------------------------------------------------ 

# 53 Make your exception class “InvalidMarks” which is thrown when marks obtained by student exceeds 100

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class InvalidMarks(Exception):
    pass
while True:
    try:
        marks = int(input("Enter your marks"))
        if marks > 100:
            raise InvalidMarks
        else:
            print(marks)
            break
    except InvalidMarks:
        print("Please enter marks below 100")
        
------------------------------------------------------------------------------------------------------------ 

# 54 WAP that accepts the values of a, b, c and d. Calculate and display ((a+d) + (b*c))/ (b*d). create user defined exception to display proper message when value of (b*d) is zero  

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class ZeroDivisionError(Exception):
    pass
a = 1
b= 2
c = 3
d = 0
try:
    if b*d == 0:
        raise ZeroDivisionError
    ans =  ((a+d) + (b*c))/ (b*d)
    print(ans)
except ZeroDivisionError:
    print("b*d ie the denominator turns out to be 0")
        
------------------------------------------------------------------------------------------------------------ 

# 55 Ask user to input an age. Raise an exception for age less than 18 , print message “ age is not valid ” & “age is valid ” if age entered is more than 18

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class InvalidAge(Exception):
    pass
try:
    age = int(input("Enter your age"))
    if age<18:
        raise InvalidAge
    print("Age is valid")
except InvalidAge:
    print("Age is not valid")
        
------------------------------------------------------------------------------------------------------------ 

# 56 Handle the FileNotFoundError exception

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
try:
    f = open("temp3.txt",'r')
except FileNotFoundError:
    print("File not found")
        
------------------------------------------------------------------------------------------------------------ 

# 57 Raise a TypeError if x is not a string  

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
x = "ev"
try:
    if not (type(x)== str):
        raise TypeError
except TypeError:
    print("Enter a string")
        
------------------------------------------------------------------------------------------------------------ 

# 58 Create class Complex , define two methods init to take real & imaginary number & method add to add real & imaginary part of complex number . print addition of real part & addition of imaginary part.

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class Complex ():
    def initComplex(self):
        self.realPart = int(input("Enter the Real Part: "))
        self.imgPart = int(input("Enter the Imaginary Part: "))            
    def display(self):
        print(self.realPart,"+",self.imgPart,"i", sep="")
    def sum(self, c1, c2):
        self.realPart = c1.realPart + c2.realPart
        self.imgPart = c1.imgPart + c2.imgPart
c1 = Complex()
c2 = Complex()
c3 = Complex()
print("Enter first complex number")
c1.initComplex()
print("First Complex Number: ", end="")
c1.display()
print("Enter second complex number")
c2.initComplex()
print("Second Complex Number: ", end="")
c2.display()
print("Sum of two complex numbers is ", end="")
c3.sum(c1,c2)
c3.display()
        
------------------------------------------------------------------------------------------------------------ 

# 59 Create class Triangle, Create object from it . The objects will have 3 attributes named a,b,c  that represent sides of triangle .Triangle class will have two methods init method to initialize the sides & method to calculate perimeter of triangle from its sides . Perimeter of triangle should be printed from outside the class

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class Triangle():
    def __init__(self,a,b,c):
        self.a = a
        self.b = b
        self.c = c
    def perimeter(self):
        return self.a+self.b+self.c
triobj = Triangle(1,2,3)
print(triobj.perimeter())
        
------------------------------------------------------------------------------------------------------------ 

# 60 Python program to append ,delete and display elements of a list using classes

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class check():
    def __init__(self):
        self.n=[]
    def add(self,a):
        return self.n.append(a)
    def remove(self,b):
        self.n.remove(b)
    def dis(self):
        return (self.n)
newlist = check()
newlist.add(5)
newlist.add(4)
newlist.add(3)
newlist.remove(4)
print(newlist.dis())
        
------------------------------------------------------------------------------------------------------------ 

# 61 Write a program  to create a class which performs basic calculator operations

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class calculator():
    def __init__(self, number1, number2):
        self.number1 = number1
        self.number2 = number2
    def addNumbers(self):
        return self.number1+self.number2
    def mulNumbers(self):
        return self.number1*self.number2
    def divNumbers(self):
        return self.number1/self.number2
    def subNumbers(self):
        return self.number1-self.number2
          
------------------------------------------------------------------------------------------------------------ 

# 62 Write a Python class named Student with two attributes student_id, student_name. Add a new attribute student_class. Create a function todisplay the entire attribute and their values in Student class.

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class Student:
    name = 'Adam'
    id = 1
def display(self):
    print(self.name)
    print(self.id)
    print(self.class_name)
s = Student()
setattr(s, 'class_name', 23)
display(s)
          
------------------------------------------------------------------------------------------------------------ 

# 63 Write a Python class to reverse a string word by word.  

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def func(str):
    list = str.split(" ")
    str = ' '.join(reversed(list))
    return str
str = "Marry had a little lamb"
print(func(str))
          
------------------------------------------------------------------------------------------------------------ 

# 64 Write a Python class which has two methods get_String and print_String. get_String accept a string from the user and print_String print the string in upper case 

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class string:
    def get_String(self):
        self.str=input("Enter a string : ")
    def print_String(self):
        print(self.str.upper())
str1 = string()
str1.get_String()
str1.print_String()
          
------------------------------------------------------------------------------------------------------------ 

# 65 Write a Python class named Circle constructed by a radius and two methods which will compute the area and the perimeter of a circle. 

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class Circle():
    def __init__(self, r):
        self.radius = r

    def area(self):
        return self.radius**2*3.14
    
    def perimeter(self):
        return 2*self.radius*math.pi
NewCircle = Circle(8)
print(NewCircle.area())
print(NewCircle.perimeter())
          
------------------------------------------------------------------------------------------------------------

# 66 rite a Python program to create a Vehicle class with max_speed and mileage instance attributes. Create a child class Bus that will inherit all of the variables and methods of the Vehicle class 

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class vehicle:
    def __init__(self, speed , milege):
        self.speed=speed
        self.milege=milege        
    def ride(self):
        print("The speed of car is " +self.speed +"  kmph and milege is "+self.milege)
p1=vehicle("120","20")
p1.ride()
print("---Child class---")
class bus(vehicle):
    pass
x=bus("140","40")
x.ride()

------------------------------------------------------------------------------------------------------------

# 67 Load a dataset using pandas : perform basic operations , data visualization using matplotlib ,seaborn etc

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
data = {
    'name': ['Xavier', 'Ann', 'Jana', 'Yi', 'Robin', 'Amal', 'Nori'],
    'city': ['Mexico City', 'Toronto', 'Prague', 'Shanghai','Manchester', 'Cairo', 'Osaka'],
    'age': [41, 28, 33, 34, 38, 31, 37],
    'py-score': [88.0, 79.0, 81.0, 80.0, 68.0, 61.0, 84.0]
}
f1=pd.DataFrame(data)
print(f1)
x=data["name"]
y=data["age"]
plt.plot(x,y)
plt.show()

------------------------------------------------------------------------------------------------------------

# 68 WAPP to push all zeros to the end of a given list. The order of elements should not change:
# Input: 0 2 3 4 6 7 9 0
# Output: 2 3 4 6 7 9 0 0

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
arr = [0,2,3,4,6,7,9,0]
for i in arr:
    if i == 0:
        arr.remove(0)
        arr.append(0)
print(arr)

------------------------------------------------------------------------------------------------------------

# 69 Write a program that accepts a comma separated sequence of words as input and prints the words in a comma separated sequence after sorting them alphabetically.
# Input: without, hello,bag, world
# Output: bag,hello,without,world

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
sen = input("Enter a comma sepreated sentence")
lis = sen.split(",")
lis.sort()
sen = ",".join(lis)
print(sen)

------------------------------------------------------------------------------------------------------------

# 70 WAP that calculates & prints value accoridng to given formula:
#  Q=Square root of [(2*C*D)/H]
#  C is 50 , H is 30. D is variable whose values should be input to program in comma separated sequence.
#  Input: 100,150,180
#  Output:18,22,24

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
d = input("Enter a comma seperated sentence: ")
list = d.split(",")
ans = []
for val in list:
    valint = int(val)
    f = math.sqrt((2*50*valint)/30)
    ans.append(str(int(f)))
print(','.join(ans))

------------------------------------------------------------------------------------------------------------

# 71 With given list L of integers , write a program that prints this L after removing duplicate values with original order preserved.
# Input: 12 24 35 24 88 120 155 88 120 155
# Output: 12 24 35 88 120 155 

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
ans = []
list = [12,24,35,24,88,120,155,88,120,155]
for i in list:
    if not i in ans:
        ans.append(i)
print(ans)

------------------------------------------------------------------------------------------------------------

# 72 Given an integer number n , define function named printDict(),which can print a dictionary where keys are numbers between 1 to n (both included) and values are square of keys . Function printDict(), does not take any arguments

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
n = int(input("Enter n"))
def printDict():
    dict = {}
    for i in range(1,n+1):
        dict[i] = i*i
    print(dict)
printDict()

------------------------------------------------------------------------------------------------------------

# 73 Python program to find the sum of the digits of an integer using while loop

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
n = int(input("Enter an integer"))
ans = 0
while n>0:
    i = n%10
    ans += i
    n //= 10
print(ans)

------------------------------------------------------------------------------------------------------------

# 74 Python program to generate the prime numbers from 1 to N 

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def print_prime(n):
    for num in range(2, n + 1):
        for i in range(2, num):
            if (num % i) == 0:
                break
        else:
            print(num)
print_prime(25)

------------------------------------------------------------------------------------------------------------

# 75 Python program to print the numbers from a given number n till 0 using recursion

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def rec(n):
    if n <= 0:
        return
    print(n)
    n -= 1
    rec(n)
rec(8)

------------------------------------------------------------------------------------------------------------

# 76 Write a Python function student_data () which will print the id of a student (student_id). If the user passes an argument student_name or student_class the function will print the student name and class.

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def student_data(student_id, **kwargs):
    print(f'\nStudent ID: {student_id}')
    if 'student_name' and 'student_class' in kwargs:
            print(f"Student Name: $ {kwargs['student_name']}")
            print(f"Student Class: $ {kwargs['student_class']}")
    elif 'student_name' in kwargs:
        print(f"Student Name: $ {kwargs['student_name']}")
student_data(student_id='SV12', student_name='Jean Garner')
student_data(student_id='SV12', student_name='Jean Garner', student_class ='V')

------------------------------------------------------------------------------------------------------------

# 77 Write a Python class to convert a roman numeral to an integer

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def roman_to_int(str):
    rom_val = {'I': 1, 'V': 5, 'X': 10, 'L': 50, 'C': 100, 'D': 500, 'M': 1000}
    ans = 0
    for i in range(len(str)):
        ans += rom_val[str[i]]
        if i>0 and rom_val[str[i]]>rom_val[str[i-1]]:
            ans -= 2*rom_val[str[i-1]]
    print(ans)
roman_to_int("IIV")

------------------------------------------------------------------------------------------------------------

# 78 Write a Python class to get all possible unique subsets from a set of distinct integers

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
import itertools
def findSubsets(s,n):
    return list(itertools.combinations(s,n))
s={1,2,3,4}
for n in range(1,len(s)):
    print(findSubsets(s,n))

------------------------------------------------------------------------------------------------------------

# 79 Write a Python class to find a pair of elements (indices of the two numbers) from a given array whose sum equals a specific target number

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
class py_solution:
  def twoSum(self, nums, target):
       lookup = {}
       for i, num in enumerate(nums):
           print(i,num)
           if target - num in lookup:
               return (lookup[target - num], i )
           lookup[num] = i
print("index1=%d, index2=%d" % py_solution().twoSum((10,20,10,40,50,60,70),50))

------------------------------------------------------------------------------------------------------------

# 80 Write a Python class to implement pow(x, n).

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import math
def pow(x,n):
    return x**n
print(pow(2,4))

------------------------------------------------------------------------------------------------------------

# 81 Write a NumPy program to convert the values of Centigrade degrees into Fahrenheit degrees and vice versa. Values are stored into a NumPy array. Sample Array [0, 12, 45.21, 34, 99.91]

import pandas as pd
import numpy as np
arr1 = np.array([1, 2, 3, 4, 5])
arr2 = arr1*1.8 + 32
print(arr2)
arr3 = (arr2-32)*5/9
print(arr3)

------------------------------------------------------------------------------------------------------------

# 82 Write a NumPy program to find the set difference of two arrays. The set difference will return the sorted, unique values in array1 that are not in array2

import pandas as pd
import numpy as np
arr1 = np.array([4,3,2,1])
arr2 = np.array([6,5,4,3])
arr3 = np.setdiff1d(arr1,arr2)
print(arr3)

------------------------------------------------------------------------------------------------------------

# 83 Write a Pandas program to create and display a DataFrame from a specified dictionary data which has the index labels. Go to the editor Sample Python dictionary data and list labels:

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf)

------------------------------------------------------------------------------------------------------------

# 84 Write a Pandas program to get the first 3 rows of a given DataFrame

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf.head(3))

------------------------------------------------------------------------------------------------------------

# 85 Write a Pandas program to select the 'name' and 'score' columns from the following DataFrame.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf.loc[:,['name','score']])
print(newdf[['name','score']])

------------------------------------------------------------------------------------------------------------

# 86 Write a Pandas program to select the specified columns and rows from a given data frame.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf.iloc[[1, 3, 5, 6], [1, 3]])

------------------------------------------------------------------------------------------------------------

# 87 Write a Pandas program to select the rows where the number of attempts in the examination is greater than 2.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf[newdf['attempts'] > 2])

------------------------------------------------------------------------------------------------------------

# 88 Write a Pandas program to count the number of rows and columns of a DataFrame.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
rows = len(newdf)
col = len(newdf.axes[1])
print("rows:", rows)
print("col:", col)

------------------------------------------------------------------------------------------------------------

# 89 Write a Pandas program to select the rows the score is between 15 and 20 (inclusive).

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf[newdf['score'].between(15, 20)])

------------------------------------------------------------------------------------------------------------

# 90 Write a Pandas program to select the rows where number of attempts in the examination is less than 2 and score greater than 15

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf[(newdf['attempts'] < 2) & (newdf['score'] > 15)])

------------------------------------------------------------------------------------------------------------

# 91 Write a Pandas program to append a new row 'k' to data frame with given values for each column. Now delete the new row and return the original DataFrame

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
newdf.loc['k'] = [ 'Suresh', 15.5,1, 'yes']
print(newdf)
newdf = newdf.drop('k')
print(newdf)

------------------------------------------------------------------------------------------------------------

# 92 Write a Pandas program to sort the DataFrame first by 'name' in descending order, then by 'score' in ascending order.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
df = newdf.sort_values(by=['name', 'score'], ascending=[False, True])
print(df)

------------------------------------------------------------------------------------------------------------

# 93 Write a Pandas program to replace the 'qualify' column contains the values 'yes' and 'no' with True and False.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
newdf['qualify'] = newdf['qualify'].map({'yes': True, 'no': False})
print(newdf)

------------------------------------------------------------------------------------------------------------

# 94 Write a Pandas program to set a given value for particular cell in DataFrame using index value.

import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
newdf = pd.DataFrame(exam_data,index=labels)
print(newdf)
# newdf._set_value('h', 'score', 20)
newdf.at['h','score'] = 20
print(newdf)

------------------------------------------------------------------------------------------------------------
