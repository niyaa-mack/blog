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


<h1>The first one:</h1>

```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```
 Number 1 shows that the expectation of the code was to count how many spaces are in a given string. The error was the if statement where the text variable needs a space when it increases but that don't happen. So my solution was to add something in the quotations and it worked.



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



This program was supposed to tell if numbers are even or odd. The issues:
<br>The input stayed as a string, so math didn’t work.
<br>The condition num % 2 < 0 wasn’t right for checking even numbers.
<br>The fix was converting the input with int(input()) and changing the condition to num % 2 == 0.




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



This program was meant to calculate factorials, but the loop stopped too early and the print statement mixed strings with integers. The fixes:
<br>Extend the loop to include the final number (range(1, num + 1)).
<br>Use proper formatting (like f‑strings) so the output combines text and numbers cleanly.



                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
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

The problem here is that the program was trying to lock the user out after three incorrect tries, but instead it kept running endlessly, allowing unlimited guesses. The issue came from the condition that only checked for attempts greater than three, which meant the program didn’t stop exactly at three. By changing the `>` to `>=`, the loop now correctly recognizes when the user has reached the third attempt and immediately ends, preventing any further inputs and making the program behave the way it was originally intended.


<p><i> And this is the end of my second blog, I hoped you enjoyed it!!!</i></p >