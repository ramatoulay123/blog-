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
This code is not working because: 
1. The input function needs to be specified as an integer rather than a string
2. The operation for 0 is less than however it should be ==.

Revised code: 

```python
print("give me a number")
# function insures only integer are being inputed for this value
n = int(input())  


for num in range(1, n):  
# If divided by 2 and nothing remains it makes it even or else odd
    if num % 2 == 0: 
        print(num, "is even.")
    else:        
        print(num, "is odd.")  
```
Now when the number you input has no remainder divided by 2 it will be even or else if not it will be odd. 

## Code # 4: 

For my fourth code it is an ifelse statement as well as a loop. The purpose of this code is to 

Here is the following code: 
```python
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result) 

```
this code is not working because: 
1. The print statement can only print strings so you need to use str() for both num and result
2. for the if statement there should not be any negative numbers so the operator is wrong and should be less than 0  

Revised code: 

```python
num = int(input("Enter an integer: "))
# Makes sure no negative number is being added 
if num < 0:
  print("No negative numbers.")
else:
  result = 1
# Add num + 1 since we wanna include the number that we input
  for i in range(1, num+1):
    result *= i   
# Can only print as a string so adding the str function helps it print
  print("Factorial of " + str(num) + "is"  + str(result)) 

```
The output of this code will be if the numbr is positive it will give you the factorial. 

## Code #5: 

For my 5th code it is a while loop and ifelse statement. The purpose of the code is to ask the user to input the correct password but you only get three attempts. 

Here is the following code: 
```python
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break 

```

This code is not working because: 
1. The first If statement prints correct password even though it equals the incorect password so you need to cj
2. For the last if statement it should be if its 3 attempts so the operator should be greater than or equal to 3.
3. After you get the correct password there should be a break so the code stops running. 

Revised code: 

```python
  attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == correct_password:
        print("Correct password!")
    # break makes the condition stop running in a loop
        break 

    else:
        print("Incorrect password")
# Minium password allowed to input is 3
    if attempts >= 3:  
        print("Too many attempts")
        break

```
This revised code allows for their to be only 3 attemps on the password and if you get it equal to the variable then it prints correct password and breaks the loop. Else if you get the incorrect password then you need to make 3 attemps and if you keep getting it wrong then the code stops.  









