# Working with Strings and Integers

Complete the following exercises to solidify your understandings of strings and integers.

## Just Strings

### 1. First & Last

If you have the strings `"First"` and `"Last"` in the following variables:

```ruby
f = "First"
l = "Last"
```

Use *only* the "string concatenation" technique to complete the following:

1. What code can you write to output the string `"FirstLast"`? f + l
2. What code can you write to output the string `"LastFirst"`? l + f
3. What code can you write to output the string `"First Last"`? f + " " + l
4. What code can you write to output the string `"Last First Last First"`? l + " " + f + " " + l + " " + f

Then repeat 1-4 using only the "string interpolation" technique.

1. What code can you write to output the string `"FirstLast"`? "#{f}#{l}"
2. What code can you write to output the string `"LastFirst"`? "#{l}#{f}"
3. What code can you write to output the string `"First Last"`? "#{f} #{l}"
4. What code can you write to output the string `"Last First Last First"`? "#{l} #{f} #{l} #{f}"

### 2. Names

Start with this string:

```ruby
name_1 = "Megan Smith"
name_2 = "Todd Park"
```

1. Can you come up with *two* ways to output just the fragment `"Megan"` from `name_1`? name_1[0, 5] and name_1[0..4]
2. Would either of your techniques from A would work to output `"Todd"` from `name_2`? Why or why not? no, because they would also capture the space between Todd and Park since they are both written to capture the first five characters of the string.
3. Write code that can output the initials of `name_2`. name_2[0] + name_2[5]

## Just Integers

Start with these numbers:

```ruby
a = 12
b = 65
c = 31
d = 98
```

1. Write code to find the average of these four numbers. (a + b + c + d) / 4
2. Find the average yourself using paper or a calculator. Is your answer different than you found in A? Why? yes. it is different because the variables are created with integers, so no fractions are recorded.
3. Say you have the operation `a + b * c / d`. What result do you get out from Ruby? What other outputs can you
get out by adding one or more pairs of parentheses to the equation? the result is 32. using (a + b) gets 24 as a result, while using (c / d) gets 12.

## Strings & Integers

### People

Say we have these people:

```ruby
a = "Ezra"
b = "Ada"
c = "Yukihiro"
d = "Grace"
```

Write code to output both the total characters in all the names together and the average length of the names.

    "#{a}#{b}#{c}#{d}"
    (a.length + b.length + c.length + d.length) / 4.0

### Happy Birthday

In our family we like to say "Happy" once for every year of your age when we say "Happy birthday!". So when you turn
four we'd say "Happy happy happy happy birthday!" Note the capitalization.

Say you have an `age` variable that holds the person's age. Write code to output the appropriate greeting.

    age = 5
    print "Happy "
    (age - 1).times do |happy|
      print "happy "
    end
    print "birthday!"

### String Compression

There's a silly compression algorithm that outputs the first letter, the number of letters in the middle,
and the last letter. So for the string `"Kalamazoo"` it'd output `"K7o"` or `"Denver"` would be `"D4r"`.
Can you write code to implement that?

    word_shorten = gets.chomp
    print word_shorten[0]
    print word_shorten.length - 2
    print word_shorten[-1]
