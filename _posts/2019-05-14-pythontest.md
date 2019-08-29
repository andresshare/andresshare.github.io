---
layout: post
title:  "Python Test"
date:   2019-05-11 18:22:08 +0530
categories: 🐍 python
---


![Python](https://media.giphy.com/media/3o6vY6L5NNr67HQW7S/giphy.gif)


Python test 🐍


**Hello**

```python
def hello():
	return "hello!!"
```

**Return the Next Number from the Integer Passed**

```python
def addition(num):
	return num + 1
```

**Area of a Triangle**
```python
tri_area = lambda b,h: (b * h)/2;
```

**Hours and Minutes to Seconds**
```python
def convert(h, m):
	return h*3600+m*60
```
**Return the Sum of Two Numbers**

```python
addition = lambda a, b : a + b
```
**Return the Remainder from Two Numbers**
```python
remainder = lambda x, y: x % y
```

**Maximum Edge of a Triangle**
```python
next_edge = lambda a, b: a+b-1
```
**To the Power of _____
**

```python
calculate_exponent = pow
```
**Minutes to Seconds**

```python
def convert(m):
	return m*60

```

**Profitable Gamble**
```python
profitable_gamble = lambda a, b, c: a*b > c
```
**Is the Number Less than or Equal to Zero?**

```python
less_than_or_equal_to_zero=lambda x:x<=0
```

**Find the Smallest Number in a List**

findSmallestNum = min

**Return the First Element in a List**
```python
get_first_value=lambda a:a[0]
```

**Name Greeting!**

```python
def hello_name(str):
    return 'Hello ' + str +'!'
```

**Multiple of 100**
```python
divisible = lambda n: n%100==0
```

**String to Integer and Vice Versa**
```python
to_int=int

to_str=str
```
**Maximum Difference**

```python
difference = lambda n:max(n)-min(n)
```
**Find the Largest Number in a List**

```python
findLargestNum = max
```
**Difference of Max and Min Numbers in List**
```python
difference_max_min = lambda l: max(l) - min(l)
```

**difference_max_min = lambda l: max(l) - min(l)**

```python
comp = lambda a, b: len(a) == len(b)
```


**Concatenate First and Last Name into One String**
```python
def concat_name(f, l):
	return l+", "+f
```
**Testing K^K == N?**

```python
k_to_k = lambda a, b: b**b == a
```

**Concatenating Two Integer Lists
**

```python
def concat(a, b):
	return a+b

```
**Check if an Integer is Divisible By Five**

```python
divisible_by_five = lambda n: n%5 == 0

```

**The 3 Programmers Problem**
```python
programmers=lambda*a:max(a)-min(a)
```

**
Is the Word Singular or Plural?**
```python

is_plural = lambda s: s[-1] == 's'
```

**Check String for Spaces**

```python
has_spaces = lambda s: ' ' in s
```

**Check if a List Contains a Given Number**

```python
check = lambda lst, el: el in lst
```

**Is the String Empty?
**
```python
is_empty = lambda s: not s

# or

is_empty = lambda a: a == ''

```
**Case Insensitive Comparison**

```python

def match(s1, s2):
	return s1 == s2.lower()

```

**Convert Number to String of Dashes**

```python
num_to_dashes = lambda x: '-'*x
```
**Is the Number Even or Odd?**

```python
isEvenOrOdd = lambda n : "odd" if n % 2 else "even"
```
**Slice of Pie**


```python
def equal_slices(t, p, e): return p*e<=t
```

**Char-to-ASCII**
```python
ctoa = ord
```
**Return the First and Last Elements in a List**

```python
first_last = lambda x: [x[0], x[-1]]
first_last = lambda lst: [lst[0], lst[-1]]
```
**Return the Last Element in a List**

```python
get_last_item = list.pop
```
**Is the Dictionary Empty?
**

```python
def is_empty(d):
	return not d
```
**
Find the Smallest and Biggest Numbers**
```python
min_max = lambda n:[min(n),max(n)]

```

**Re-Form The Word**
```python
get_word=lambda l,r:l.title()+r
get_word = lambda l, r: l.capitalize()+r

```
**No Conditionals?**
```python
flip = lambda a:not a
#or
def flip(y):
	return y ^ 1

```

**Stack the Boxes**
```python
stack_boxes = lambda n: n**2
```

**Sort Numbers in Ascending Order**


```python
sort_nums_ascending = sorted
```
**
Check if the Same Case**

```python
same_case = lambda s: s.islower() or s.isupper()
```

**Find the Index**

```python
find_index = list.index
```
**Reverse the Case**

```python
reverse_case = str.swapcase
```
**Truthy or Falsy?**

```python
is_truthy = lambda x: 1 if x else 0
```
**Hashes and Pluses**


```python
hash_plus_count = lambda s: [s.count(i) for i in '#+']
```


**Limit a Number's Value**

```python
limit_number=lambda a,b,c:sorted([a,b,c])[1]
#or
def limit_number(x, y, z):
	return y if x < y else z if x > z else x
```


**Next Element in Arithmetic Sequence**
```python
next_element = lambda l: l[1]-l[0]+l[-1]
```

#50

**Find the Total Number of Digits the Given Number Has**


```python
find_digit_amount = lambda n: len(str(n))
```


**Missing Third Angle
**
```python
missing_angle = lambda a, b: 'acute' if a+b > 90 else 'obtuse' if a+b < 90 else 'right'
```


**
Find the Index (Part 1)**

```python
search=lambda l,i:-1if i not in l else l.index(i)
```

**Count Instances of a Character in a String**

```python
char_count = lambda x,y: y.count(x)
```


**Add, Subtract, Multiply or Divide?**

```python
def operation(a, b):
	return {a+b: "added", a-b: "subtracted", a*b: "multiplied", a/b: "divided"}.get(24)

```
**Find the Index (Part 2)**

```python
search=lambda l,i:-1 if i not in l else l.index(i)
```

**Count Syllables**


```python
def number_syllables(w):
	return 1 + w.count('-')
```



**Scoring System**

```python
def calculate_scores(txt):
    return [txt.count(c) for c in "ABC"]

```

**Volume of a Box
**

```python
animals = lambda c, m, p: c * 2 + m * 4 + p * 4

```
**Volume of a Box**


```python
def volume_of_box(sizes):
	x,y,z=sizes.values()
	return x*y*z
```


**String or Integer?**

```python
def int_or_string(var):
	return type(var).__name__

```

**Reverse a List**

```python
reverse = lambda l: l[::-1]
```



**Word Endings
**


```python
add_ending = lambda l, e: [s+e for s in l]
```


**Same Number of Unique Elements
**
```python
same = lambda a1, a2: len(set(a1)) == len(set(a2))
```

**Check if Number is within a Given Range**

```python
is_in_range = lambda n, r: r["min"] <= n <= r["max"]
```

**Basic Statistics: Mean**
```python
mean=lambda n:round(sum(n)/len(n),1)

```

**Unlucky 13**
```python
unlucky_13=lambda l:[n for n in l if n%13]
```
**Total Number of Unique Characters**

```python
count_unique = lambda a, b: len(set(a+b))
count_unique = lambda s1, s2: len(set(s1 + s2))
```
**Calculate Determinant of a 2x2 Matrix**

```python
calc_determinant = lambda m:m[0][0]*m[1][1]-m[0][1]*m[1][0]

def calc_determinant(matrix):
	[a,b],[c,d] = matrix
	return a*d - b*c
```


**Additive Inverse**

```python
additive_inverse = lambda l: [a*-1 for a in l]
additive_inverse = lambda lst: [-x for x in lst]
```
**Sum of Cubes**

```python
sum_of_cubes = lambda n:sum(i**3 for i in n)
```
**Recursion: Array Sum**
```python
sum_recursively = lambda x: sum(x)
```
**Get Word Count**

```python
count_words = lambda t:t.count(" ")+1

```
**Extract City Facts**


```json
`city_facts({
  name: "Paris",
  population: "2,140,526",
  continent: "Europe"
}) ➞ "Paris has a population of 2,140,526 and is situated in Europe"

city_facts({
  name: "Tokyo",
  population: "13,929,286",
  continent: "Asia"
}) ➞ "Tokyo has a population of 13,929,286 and is situated in Asia"`
```


```python
def city_facts(x):
    return x['name'] + " has a population of " + x['population'] + " and is situated in " + x['continent']
```

```python
def city_facts(city):
	return '{name} has a population of {population} and is situated in {continent}'.format(**city)
```

**Say "Hello" Say "Bye"**

```python
say_hello_bye = lambda n, b: 'Hello '+n.title() if b else 'Bye '+n.title()
```

**Valid Zip Code
**

```python

def is_valid(z):
	return z.isdigit()

```
**
Hitting the Jackpot**


```python

test_jackpot = lambda x: len(set(x)) == 1
```
**
Same ASCII?**

```python
def same_ascii(a, b):
	return sum(map(ord, a)) == sum(map(ord, b))
```

**Palindrome?
**
```python
def is_palindrome(txt):
	return txt == txt[::-1]
```

**
Reverse Coding Challenge #3
**


```python
def mystery_func(lst, n):
  return [i % n for i in lst]

```

**Remove the First and Last Characters
**
```python
def remove_first_last(txt):
	return txt[1:-1] or txt
```

**Check if One List is Subset of Another**


```python
def subset(l1, l2):
	return all([n in l2 for n in l1])
```

```python
def subset(lst1, lst2):
	return set(lst1) <= set(lst2)

```

**Capture the Rook**

```python
def can_capture(r):
	return r[0][0] in r[1] or r[0][1] in r[1]

```

**Semantic Versioning**

```python
def retrieve_major(v):
    return v.split('.')[0]


def retrieve_minor(v):
	return v.split('.')[1]


def retrieve_patch(v):
    return v.split('.')[2]
```


**Convenience Store
**
```python
def change_enough(c, a):
	return a<=c[0]*.25+c[1]*.1+c[2]*.05+c[3]*.01
```
**Hurdle Jump**

```python
def hurdle_jump(x, p):
	return x == [] or p >= max(x)

```

**Between Words**

```python
def is_between(f, l, w):
	return sorted([f,l,w])[1]==w
```

**Odd Up, Even Down**

```python
transform = lambda l: [n+1 if n % 2 else n-1 for n in l]
```
**Check if a String Contains only Identical Characters**
```python
def is_identical(s):
	return s[::-1] == s
```
```python

is_identical = lambda s:s == len(s)* s[0]
```

**Online Shopping**
```python
def free_shipping(o):return sum(o.values())>50
```

**Exists a Number Higher?**

```python
def exists_higher(lst, n):
	return max(lst or [-1]) >= n
```
**Increment to Top**
```python
def increment_to_top(l):
	return sum(max(l)-i for i in l)
```

**Even Odd Partition**

```python
even_odd_partition = lambda l:[[i for i in l if not i%2],[i for i in l if i%2]]
```
**
Find the Bug: Checking Even Numbers**

```python
def check_all_even(lst):
  return all(x%2 == 0 for x in lst)
```
**
Smaller String Number**
```python

def smaller_num(n1, n2):
	return min(n1,n2)
```
**
Remove None from a List**

```python
remove_none = lambda l: [i for i in l if i != None]
```
**Repeat the Same Item Multiple Times**

```python
def repeat(i, t):
	return [i]*t
```

**Omnipresent Value**

```python
def is_omnipresent(lst, val):
	return all(val in i for i in lst)
```
**
Spelling it Out**
```python

def spelling(t):
	return [t[0:i] for i in range(1,len(t)+1)]
```
**List from Comma-Delimited String**
```python
def to_array(t):
	return t.split(", ") if len(t) else []
```
**Repeating Letters N Times**

```python
def repeat(t, n):
	return ''.join([c*n for c in t])
```

**Generate a Countdown of Numbers in a List**

```python
def countdown(n):
	return [n-i for i in range(n+1)]
```

**Filter Repeating Character Strings**

```python
def identical_filter(lst):
	return [i for i in lst if i[1:]==i[:-1]]

```