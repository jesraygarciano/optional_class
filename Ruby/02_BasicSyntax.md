# BasicSyntax

1. Hello World

```Ruby
# line break
puts "hello world(puts)"

# no line break
print "hello world!"
print "hello world!"
```

2. Variables

```Ruby
text = "This is text"
puts text

text = "Update !!!"
puts text
```

3. Comment out

```Ruby
# This is comment

=begin
comment
comment
comment
=end
```

4. Operators

```Ruby

puts 1 + 1
puts 2 - 1
puts 2 * 2
puts 3 / 2

```

5. If

```Ruby
time = 12
if time > 12
    puts 'Good afternoon'
else
    puts 'Good morning'
end

type = 3
if type == 1
    puts 'BaseBall'
elsif type == 2
    puts 'Soccer'
else
    puts 'BasketBall'
end
```

6. for

```Ruby
for i in range(0, 10):
  print(i)
```

7. while

```Ruby
count = 0

while count < 10:
    print(count)
    count += 1

```

8. Function

```Ruby

def printHello
    puts "Hello World From Function"
end

# use function
printHello


def printName(name)
    puts "My name is " + name
end

# use function
printName("SeedKun")
```