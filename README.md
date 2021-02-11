# Python_assignment

## Question 1:
```python
n = int(input())
for i in range(1,11):
    if n >0:
        print(i*n)
        i+=1
```
## Question 2:
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
```python
from num2words import num2words

n = int(input("Enter a number : "))
print("In words : ",num2words(n))
```
## Question 4:
```python
arr = list(map(int,input().split()))
def func(arr):
    print(sum(arr))
        
func(arr)
```
## Question 7:
```python
n = list(map(int,input().split()))
print(sum(n))
```
## Question 8:
```python
n = list(map(int,input().split()))
sum_num = sum(n)
print("sum of num is : ",sum_num)
print("average of num is : ",sum_num/2)
```

