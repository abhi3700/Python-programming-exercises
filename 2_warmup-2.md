### Warmup-2 > string_times

**Question**:
Given a string and a non-negative int n, return a larger string that is n copies of the original string.

**Check for these cases**:
```
string_times('Hi', 2) → 'HiHi'
string_times('Hi', 3) → 'HiHiHi'
string_times('Hi', 1) → 'Hi'
```

**Solution**:
```python
def string_times(str, n):
    if(n>0):
        print(n * str)
    else:
        return -1

string_times('Hi', 2) #→ 'HiHi'
string_times('Hi', 3) #→ 'HiHiHi'
string_times('Hi', 1) #→ 'Hi'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > front_times 

**Question**:
Given a string and a non-negative int n, we'll say that the front of the string is the first 3 chars, or whatever is there if the string is less than length 3. Return n copies of the front;

**Check for these cases**:
```
front_times('Chocolate', 2) → 'ChoCho'
front_times('Chocolate', 3) → 'ChoChoCho'
front_times('Abc', 3) → 'AbcAbcAbc'
```

**Solution**: 
```python
def front_times(str, n):
    if(n>0 and str != ""):
        front = str[0:3]
        print(n * front)
    else:
        return -1

front_times('Chocolate', 2) #→ 'ChoCho'
front_times('Chocolate', 3) #→ 'ChoChoCho'
front_times('Abc', 3) #→ 'AbcAbcAbc'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > string_bits 

**Question**:
Given a string, return a new string made of every other char starting with the first, so "Hello" yields "Hlo".

**Check for these cases**:
```
string_bits('Hello') → 'Hlo'
string_bits('Hi') → 'H'
string_bits('Heeololeo') → 'Hello'
```

**Solution**: 
```python
def string_bits(str):
    nstr = ""
    for i in range(0,len(str),2):   # e.g. len = 5, so, i = 0,2,4
        nstr += str[i]
    print(nstr)

string_bits('Hello') #→ 'Hlo'
string_bits('Hi') #→ 'H'
string_bits('Heeololeo') #→ 'Hello'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > string_splosion 

**Question**:
Given a non-empty string like "Code" return a string like "CCoCodCode".

**Check for these cases**:
```
string_splosion('Code') → 'CCoCodCode'
string_splosion('abc') → 'aababc'
string_splosion('ab') → 'aab'
```

**Solution**:
```python
def string_splosion(str):
    nstr = ""
    for i in range(len(str)):
        nstr += str[:i+1]     # gives 'CCoCodCode'
        #nstr += str[0:len(str)-i]  # gives 'CodeCodCoC'
    print(nstr)

string_splosion('Code') #→ 'CCoCodCode'
string_splosion('abc') #→ 'aababc'
string_splosion('ab') #→ 'aab'
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > array_count9 

**Question**:
Given an array of ints, return the number of 9's in the array.

**Check for these cases**:
```
array_count9([1, 2, 9]) → 1
array_count9([1, 9, 9]) → 2
array_count9([1, 9, 9, 3, 9]) → 3
```

**Solution**: 
```python
def array_count9(nums):
    count = 0
    for num in nums:
        if(num == 9):
            count = count + 1
    print(count)
    
array_count9([1, 2, 9]) #→ 1
array_count9([1, 9, 9]) #→ 2
array_count9([1, 9, 9, 3, 9]) #→ 3
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > array_front9   

**Question**:
Given an array of ints, return True if one of the first 4 elements in the array is a 9. The array length may be less than 4.

**Check for these cases**:
```
array_front9([1, 2, 9, 3, 4]) → True
array_front9([1, 2, 3, 4, 9]) → False
array_front9([1, 2, 3, 4, 5]) → False
array_front9([1, 2, 3]) #→ False
```

**Solution**: 
```python
def array_front9(nums):
  bool = False
  end = len(nums)
  if end > 4:
    end = 4
  
  for i in range(end):
    if nums[i] == 9:
      bool = True   
      print(bool)
      
  if (bool != True):    
    print(False)
      
array_front9([1, 2, 9, 3, 4]) #→ True
#print("\n")
array_front9([1, 2, 3, 4, 9]) #→ False
#print("\n")
array_front9([1, 2, 3, 4, 5]) #→ False
#print("\n")
array_front9([1, 2, 3]) #→ False

# Remarks: here, we introduced this parameter, otherwise the program would return False along with True.
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > array123  

**Question**:
Given an array of ints, return True if the sequence of numbers 1, 2, 3 appears in the array somewhere.

**Check for these cases**:
```
array123([1, 1, 2, 3, 1]) → True
array123([1, 1, 2, 4, 1]) → False
array123([1, 1, 2, 1, 2, 3]) → True
```

**Solution**:
```python
def array123(nums):
    max = len(nums)
    bool = False # defined for expected output, otherwise it will print False along with True.
    for i in range(max):
      if nums[i:i+3] == [1,2,3]:
        bool = True
        print(bool)
    if bool != True:
      print(False)
    
array123([1, 1, 2, 3, 1]) #→ True
print("\n")
array123([1, 1, 2, 4, 1]) #→ False
print("\n")
array123([1, 1, 2, 1, 2, 3]) #→ True
```
#----------------------------------------#

#----------------------------------------#
### Warmup-2 > string_match  

**Question**:
Given 2 strings, a and b, return the number of the positions where they contain the same length 2 substring. So "xxcaazz" and "xxbaaz" yields 3, since the "xx", "aa", and "az" substrings appear in the same place in both strings.

**Check for these cases**:
```
string_match('xxcaazz', 'xxbaaz') → 3
string_match('abc', 'abc') → 2
string_match('abc', 'axc') → 0
```

**Solution**: 
```python
def string_match(str1, str2):
  # define the minimum length of the strings
  short = min(len(str1), len(str2))
  #define the count
  count = 0
  
  for i in range(short):
    if str1[i:i+2] == str2[i:i+2]:
      count = count + 1
      print(str1[i:i+2]) # prints the 2 substring
  
  print(count)
  
string_match('xxcaazz', 'xxbaaz') #→ 3
print("\n")
string_match('abc', 'abc') #→ 2
print("\n")
string_match('abc', 'axc') #→ 0
```
#----------------------------------------#

#----------------------------------------#
