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
## Question 11:
 Filter the list of names which starts with 's'.
```python
names = list(input().split())
for i in range(len(names)):
    if names[i][0].lower() == 's':
        print(names[i])
    else:
        continue
```
## Question 12:
Find the average of some list of values.
```python
l = list(map(int,input().split()))
for i in range(len(l)):
    total = sum(l) / len(l)
print(total)
```
## Question 13:
WAP which doubles every element of a list.
```python
l = list(map(int,input().split()))
for i in range(len(l)):
    sq = l[i]*2
    print(sq)
```
## Question 14:
WAP to swap case the strings of a list.
```python
newstring =''
names = list(input().split())
for i in range(len(names)):
    if names[i].isupper():
        newstring+=(names.lower())
    else:
        newstring+=(names.upper())
print(names)
```
## Question 15:
Calculating the sum of the numbers from 1 to 100.
```python
total=0
for i in range(1,101):
    total+=i
print(total)
```
## Question 16:
Imagine an accounting routine used in a book shop. It works on a list with sublists, which look like this:<br>
Order Number Book Title and Author Quantity Price per Item<br>
34587 Learning Python, Mark Lutz 4 40.95<br>
98762 Programming Python, Mark Lutz 5 56.80<br>
77226 Head First Python, Paul Barry 3 32.95<br>
88112 Einführung in Python3, Bernd Klein 3 24.99<br>
Write a Python program, which returns a list with 2-tuples. Each tuple consists of a the order number and the product of the price per items and the quantity. The product should be increased by 10,- € if the value of the order is smaller than 100,00 €.<br>
Write a Python program using lambda and map.
```python
def orderzip(onum,quantity,price):
    total_price = [quantity[x]*price[x] for x in range(len(price))]
    total_price = list(map(lambda x : x+10 if x < 100 else x,total_price))
    return list(zip(onum,total_price))
    
order_number = (34587, 98762, 77226, 88112)

quantity = (4,5,3,3)

price = (40.95,56.80,32.95,24.99)


print(orderzip(order_number,quantity,price))
```
