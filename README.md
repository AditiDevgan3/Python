# Python_assignment

## Question 1:
WAP in python to print table of a number up to 12.
```python
n = int(input())
for i in range(1,11):
    if n >0:
        print(i*n)
        i+=1
```
## Question 2:
WAP to display all prime numbers up to a given number.
```python
lower = int(input("Enter lower range: "))  
upper = int(input("Enter upper range: "))  
  
for num in range(lower,upper + 1):  
   if num > 1:  
       for i in range(2,num):  
           if (num % i) == 0:  
               break  
       else:  
           print(num)
```
## Question 3:
WAP to input a number from user and write it in words.
```python
from num2words import num2words

n = int(input("Enter a number : "))
print("In words : ",num2words(n))
```
## Question 4:
WAP to define a function which adds arbitrary numbers.
```python
arr = list(map(int,input().split()))
def func(arr):
    print(sum(arr))
        
func(arr)
```
## Question 5:
WAP to show the use of keywords arguments in python.
```python
def func(a,b,c):
    print(max(a,b,c))
       
func(c=5,a=6,b=9)
```
## Question 6:
WAP to show the use of arbitrary keyword arguments in python.
```python
def func(**kwargs):
    for i in kwargs:
        print("key = {} : value = {}".format(i,kwargs[i]))
       
func(b="Kamikaze",a="kaydee",c="blackbess")
```
## Question 7:
WAP to read a number and print sum of its digits.
```python
n = list(map(int,input().split()))
print(sum(n))
```
## Question 8:
WAP to read a list of numbers and print the sun and average.
```python
n = list(map(int,input().split()))
sum_num = sum(n)
print("sum of num is : ",sum_num)
print("average of num is : ",sum_num/2)
```
## Question 9:
WAP to read a string from user and print it back after swap case.
```python
String = input()
print(String.swapcase())
```
## Question 10:
WAP to read a paragraph from user , calculate number of words, vowels and consonants.
```python
String = input()
Vowels = 0
Consonant = 0
words = 0
for i in range(len(String)):
    ch = String[i]
    if ( (ch >= 'a' and ch <= 'z') or (ch >= 'A' and ch <= 'Z') ):
        ch = ch.lower()
        if (ch == 'a' or ch == 'e' or ch == 'i' 
                        or ch == 'o' or ch == 'u'): 
            Vowels += 1
        else: 
            Consonant += 1
            
print("Number of Vowels in the string are: ",Vowels)
print("Number of Consonant in the string are: ",Consonant)
print("Number of Words in the string are: ",len(String.split()))
```
