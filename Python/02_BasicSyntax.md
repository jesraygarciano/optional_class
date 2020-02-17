# BasicSyntax

1. Hello World

```Python
print("Hello World")
```

2. Variables

```Python
text = "This is text"
print(text)

text = "Update !!!"
print(text)
```

3. Comment out

```Python
# This is comment
```

3.1. Indention

```Python

#Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important. Python uses to indicate a block of code.


```

```Python
text = "This is text"
print(text)

text = "Update !!!"
print(text)
```



4. operations

```Python

print(1 + 1)
print(2 - 1)
print(2 * 2)
print(3 / 2)

print(3 ** 2)
print(3 // 2)

```

5. String operations

```Python
print ("hello"+"world")
print ("hello" * 3)
```

6. User input

```Python
name=input("Input your name")
print("Hello " + name)
```

7. If

```Python
score = 90
if score > 80:
    print("Great!")
elif score > 60:
    print("Good!")
else:
    print("OK")
```

8. for loop

```Python
for i in range(0, 10):
  print(i)
```

9. while loop

```Python
count = 0

while count < 10:
    print(count)
    count += 1

```

## sample codes

```Python

print("Hello World")

# # is comment out

# variables
text = "This is text"
print(text)

text = "Updated !!!"
print(text)

# There are no constants. But there is a rule that uppercase variables are treated as constants
TEXT = "This is constants"
print(TEXT)

# operations
print(1 + 1)
print(2 - 1)
print(2 * 2)
print(3 / 2)

# Exponentiation
print(3 ** 2)

# Division (only integer results are returned)
print(3 // 2)

# Character manipulation
print("Hello" + "World")
print("Hello" * 5)


# if statement
age = 20
if age > 10:
  print("older than 10 years old")

if age < 20:
  print("younger than 20 years old")
else:
  print("older than 20 years old"")


# User input
name = input("Please tell me your name")
print("My name is " + name)

# for loop
for i in range(0,10):
  print(i)

print("text")


# while loop

count = 0

while count < 10:
    print(count)
    count += 1

```