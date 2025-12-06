<p>Welcome back to another blog post by SM. This time we are talking about debugging. Debugging is basically 
troubleshooting to me but the exact definition is the process of finding and resolving errors, or "bugs," in software code. 
In class we did a debugging exercise where my teacher gives us a error code and we fix the 
code and says what was the issue and how to fix the issue.</p>

<h1> The example given: </h1>


```python
temperature = 75

if temperature > 80:
    print("It's hot")
elif temperature > 50:
    print("It's temperate")
elif temperature < 0:
    print("It's cold")
```


**<h1>The first one:</h1>**

```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```

<p> Number 1 shows that the expectation of the code was to count how many spaces are in a given string. The error was the if statement where the text variable needs a space when it increases but that don't happen. So my solution was to add something in the quotations and it worked. </p>



<h1> Number 2:</h1>

```python
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```



<p> Number 2 was expected to determine if the number 1 to how ever much they input are even or odd. The problem I found was the first line is a print not an input and the input default is an string so whatever number the user inputs it will be an error due to it not being converted to a integer. The solution is to put an int infront of the input and in the if statement change it to less than and equal to so the code could work. </p>



<h1> Number 3: </h1>

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



<p> Number 3 was used to calculate the factorial of a given number but it didn't work so the problem of the code was the range did not increase by 1. The way I fixed the code was to add a curly brackets for the num and result on the last line of code and to increase by 1 for the range. The code is not going to work if when the range is met the result don't go up by 1. </p>



<h1> Number 4:</h1>

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

<p>And finally number 4 was asking the user to enter the correct password but they only get three attempts. The code was messed up by giving the user more than 3 three attempts. So I had to add the equal sign to the greater than sign to make the attempts stop at 3. </p>


<p><i> And this is the end of my second blog, I hoped you enjoyed it!!!</i></p >