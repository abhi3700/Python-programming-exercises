### Warmup-1 > sleep_in

**Question**:
The parameter weekday is True if it is a weekday, and the parameter vacation is True if we are on vacation. We sleep in if it is not a weekday or we're on vacation. Return True if we sleep in.

**Check for these cases**:
```
sleep_in(False, False) → True 
sleep_in(True, False) → False
sleep_in(False, True) → True
```

**Solution**: 
```python
def sleep_in(weekday, vacation):
    if(not weekday or vacation):
        print("True")
    else:
        print("False")

sleep_in(False, False) #→ True
sleep_in(True, False) #→ False
sleep_in(False, True) #→ True
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > monkey_trouble

**Question**:
We have two monkeys, a and b, and the parameters a_smile and b_smile indicate if each is smiling. We are in trouble if they are both smiling or if neither of them is smiling. Return True if we are in trouble.

**Check for these cases**:
```
monkey_trouble(True, True) → True
monkey_trouble(False, False) → True
monkey_trouble(True, False) → False
```

**Solution**: 
```python
def monkey_trouble(a_smile, b_smile):
    if a_smile and b_smile:
        print("True")
    elif not a_smile and not b_smile:
        print("True")
    else:
        print("False")
        
monkey_trouble(True, True) #→ True
monkey_trouble(False, False) #→ True
monkey_trouble(True, False) #→ False
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > sum_double 

**Question**:
Given two int values, return their sum. Unless the two values are the same, then return double their sum.

**Check for these cases**:
```
sum_double(1, 2) → 3
sum_double(3, 2) → 5
sum_double(2, 2) → 8 
```

**Solution**: 
```python
def sum_double(a, b):
    # Store the sum in a local variable
      sum = a + b
      if (a == b):
        sum = sum * 2
      print(sum)
    
#Alternative solution - 
#    if (a == b):
#        print((a+b)*2)
#    else:
#        print(a+b)

sum_double(1, 2) #→ 3
sum_double(3, 2) #→ 5
sum_double(2, 2) #→ 8
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > diff21 

**Question**:
Given an int n, return the absolute difference between n and 21, except return double the absolute difference if n is over 21.

**Check for these cases**:
```
diff21(19) → 2
diff21(10) → 11
diff21(21) → 0
```

**Solution**:
```python
def diff21(n):
    diff = 21-n
    if n>21:
        diff = diff*2
    print(diff)

diff21(19) #→ 2
diff21(10) #→ 11
diff21(21) #→ 0
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > parrot_trouble

**Question**:
We have a loud talking parrot. The "hour" parameter is the current hour time in the range 0..23. We are in trouble if the parrot is talking and the hour is before 7 or after 20. Return True if we are in trouble.

**Check for these cases**:
```
parrot_trouble(True, 6) → True
parrot_trouble(True, 7) → False
parrot_trouble(False, 6) → False
```

**Solution**:
```python
def parrot_trouble(talking, hour):
    if(talking and (hour<7 or hour>20)):
        print("True")
    else:
        print("False")
        
parrot_trouble(True, 6) #→ True
parrot_trouble(True, 7) #→ False
parrot_trouble(False, 6) #→ False
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > makes10 

**Question**:
Given 2 ints, a and b, return True if one if them is 10 or if their sum is 10.

**Check for these cases**:
```
makes10(9, 10) → True
makes10(9, 9) → False
makes10(1, 9) → True
```

**Solution**: 
```python
def makes10(a, b):
    if((a == 10) or (b == 10) or (a+b == 10)):
        print("True")
    else:
        print("False")
        
makes10(9, 10) #→ True
makes10(9, 9) #→ False
makes10(1, 9) #→ True
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > near_hundred 

**Question**:
Given an int n, return True if it is within 10 of 100 or 200. Note: abs(num) computes the absolute value of a number.

**Check for these cases**:
```
near_hundred(93) → True
near_hundred(90) → True
near_hundred(89) → False
```

**Solution**: 
```python
def near_hundred(n):
    diff1 = abs(100-n)
    diff2 = abs(200-n)
    if(diff1 <= 10 or diff2 <=10):
        print("True")
    else:
        print("False")
        
near_hundred(93) #→ True
near_hundred(90) #→ True
near_hundred(89) #→ False
near_hundred(190) #→ True
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > pos_neg 

**Question**:
Given 2 int values, return True if one is negative and one is positive. Except if the parameter "negative" is True, then return True only if both are negative.

**Check for these cases**:
```
pos_neg(1, -1, False) → True
pos_neg(-1, 1, False) → True
pos_neg(-4, -5, True) → True
```

**Solution**: 
```python
def pos_neg(a, b, negative):
    if negative: 
        print(a<0 and b<0)
    else:
        print((a<0 and b>0) or (a>0 and b<0))
        
pos_neg(1, -1, False) #→ True
pos_neg(-1, 1, False) #→ True
pos_neg(-4, -5, True) #→ True
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > not_string 

**Question**:
Given a string, return a new string where "not " has been added to the front. However, if the string already begins with "not", return the string unchanged.

**Check for these cases**:
```
not_string('candy') → 'not candy'
not_string('x') → 'not x'
not_string('not bad') → 'not bad'
```

**Solution**: 
```python
def not_string(str):
    if(len(str) >= 3 and str[0:3] == 'not'):
        print(str)
    else:
        print('not '+str)
        
# str[:3] goes from the start of the string up to but not
# including index 3
    
not_string('candy') #→ 'not candy'
not_string('x') #→ 'not x'
not_string('not bad') #→ 'not bad'
```
#----------------------------------------#

#----------------------------------------
### Warmup-1 > missing_char 

**Question**:
Given a non-empty string and an int n, return a new string where the char at index n has been removed. The value of n will be a valid index of a char in the original string (i.e. n will be in the range 0..len(str)-1 inclusive).

**Check for these cases**:
```
missing_char('kitten', 1) → 'ktten'
missing_char('kitten', 0) → 'itten'
missing_char('kitten', 4) → 'kittn'
```

**Solution**:
```
def missing_char(str, n):
    front  = str[:n]  # upto str[n-1] 
    back = str[n+1:]  # from n+1 to end of the string
    print(front + back)
    
missing_char('kitten', 1) #→ 'ktten'
missing_char('kitten', 0) #→ 'itten'
missing_char('kitten', 4) #→ 'kittn'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > front_back_reverse

**Question**:
Given a string, find the reversed string.

**Check for these cases**:
```
front_back_rev('code') → 'eodc'
front_back_rev('a') → 'a'
front_back('ab') → 'ba'
```

**Solution**:
```python
def front_back_rev(str): 
    rstr = ""  # initialized the unused variable.
    for i in range(len(str)):
        rstr += str[(len(str)-1)-i]
    print(rstr)

front_back_rev('code') #→ 'edoc'
front_back_rev('a') #→ 'a'
front_back_rev('ab') #→ 'ba'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > front_back

**Question**:
Given a string, return a new string where the first and last chars have been exchanged.

**Check for these cases**:
```
front_back('code') → 'eodc'
front_back('a') → 'a'
front_back('ab') → 'ba'
```

**Solution**:
```python
def front_back(str):
    if(len(str)<=1):  # if the string is of single character, print the same string.
        print(str)
    else:
        front = str[0]  # 1st character
        mid = str[1:len(str)-1]
        last = str[len(str)-1] # last character
        new_str = last + mid + front # string added in reverse order, with middle part same as previous.
        print(new_str)

front_back('code') #→ 'eodc'
front_back('a') #→ 'a'
front_back('ab') #→ 'ba'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-1 > front3

**Question**:
Given a string, we'll say that the front is the first 3 chars of the string. If the string length is less than 3, the front is whatever is there. Return a new string which is 3 copies of the front.

**Check for these cases**:
```
front3('Java') → 'JavJavJav'
front3('Chocolate') → 'ChoChoCho'
front3('abc') → 'abcabcabc'
```

**Solution**: 
```python
def front3(str):
    if(len(str)>=3): # if the same string has 3 or more characters string, print the required string
        print(3 * str[0:3])  # str[0:3] means from str[0] to str[2]
    else:          # if the string has less than 3 character string, print the same string.
        print(3*str)

front3('Java') #→ 'JavJavJav'
front3('Chocolate') #→ 'ChoChoCho'
front3('abc') #→ 'abcabcabc'
```
#----------------------------------------#

#----------------------------------------#
