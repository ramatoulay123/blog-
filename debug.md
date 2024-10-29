# Finding the Bug 
## How I debugged the impossible 

<br> 

Debugging is the act of using your problem solving skills in order to determine an error in a following code. 


In my full stack development class I had the oppurtunity to debug a code given to me and figure out what the problem was. This made me also come up with a solution to my issue.




## Code # 1: 

For my first code I was given it was an elif code and my Job was to figure out what the issue was and a solution to the problem.

Here is the following code:
```python
teampuature = 75

if teampuature > 80:
   print("its hot")
elif teampuature > 50:
   print("its temperate)
elif teampuature < 0:
   print("Its cold") 
```
The purpose of this code was to determine wheter the teampuature is hot, temperate, or cold. 

However the error in this code was that it did not account for numbers between 0 and 50, since for both of the elif statements the operation sign should be changed in order for those numbers. 

The way to fix this is by changing the final elif statement to else so that anything less than 50 is considered cold. 

Revised code: 

```python
teampuature = 75

if teampuature > 80:
   print("its hot")
elif teampuature > 50:
   print("its temperate)
else:
   print("Its cold") 
```

This fixes the bug by accounting for the numbers that are less than 50 degrees. 


## Code # 2: 
<br> 
For my second code I was given a for loop and the purpose of the code is to count the spaces in a given string. 

Here is the following code: 
```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count) 
```
The error of this code was that it was not counting the amount of spaces at all rather when you run the code it will give you 0. 

The way to fix this is by putting a space between the two quotation marks after the == sign. 

Revised code: 

```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == " ":
       count += 1

print(count) 
```

Now when you run it the output will be 4 since based on the text there is 4 spaces in between each letter. 


## Code # 3: 
<br> 
For my third code I was given a for statement to determine if a number is Even or odd. 

Here is the following code: 
```python
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")  
```












