# Python ChatGPT Exercises

### I asked ChatGPT to create some intermediate-level Python tasks for me, as if they were an IT recruiter. I treated it as a test of my skills. In the near future I will ask ChatGPT for more tasks of increasing difficulty level.



#### 1. Write a program that calculates the arithmetic mean of a list of numbers.


```
def num_mean(lst):
    sum = 0
    for number in lst:
        sum += number
    average = sum/len(lst)
    return average
    



lst = input("Enter a comma-separated list of numbers: ")

lst = lst.split(",")
for i in range(len(lst)):
    lst[i] = float(lst[i].strip())

num_mean(lst)
```


#### 2. Write a program that prompts the user for the name of a text file, opens it, and counts the occurrences of each word in the text.
```

words = input("Enter the sentence you want to count the number of words: ")
lst = words.replace(',',' ').replace('.',' ').split()
print(lst)

def count_wrd(list):
    sum=0
    for i in range(len(list)):
        sum+=1
    return sum

count_wrd(lst)
```

#### 3. Write a program that prompts the user for a list of numbers and then removes all odd numbers from it.

```
def cnt(lst):
    par = []
    for i in range(len(lst)):
        if lst[i] % 2 == 0:
            par.append(lst[i])
    return par

while True:
    try:
        lst = input("Enter a comma-separated list of numbers: ")
        lst = lst.split(",")
        lst = [float(elem) for elem in lst]
        break
    except ValueError:
        print("Invalid input, please enter a valid comma-separated list of numbers")
        continue
    
print(cnt(lst))
```


#### 4. Write a program that prompts the user for a list of surnames and sorts them alphabetically. The program should also allow for reverse sorting.
```
while True:
    try:
        lst = input("Enter a comma-separated list of second names: ")
        srt = input("Choose sorting: From A to Z type A, from Z to A type Z: ")
        lst = [elem.strip() for elem in lst.split(',')]
        srt = srt.lower()
        
        if len(srt) == 1 and (srt == 'a' or srt == 'z'):
            
            if srt == 'a':
                
                lst_sorted = sorted(lst, key=str.lower)
                break
            
            else:
                
                lst_sorted = sorted(lst, key=str.lower, reverse=True)
                break
            
        else:
            print("Invalid sorting choice. Please enter 'A' or 'Z'.")
            continue
    except ValueError:
        print('Invalid input. Please enter a comma-separated list of second names.')
        continue      

print(lst_sorted)
```

#### 5. Write a program that prompts the user for two dates and calculates the number of days between them.

```
from datetime import datetime

date_format = "%Y-%m-%d"

date1_str = input("Podaj pierwszą datę w formacie RRRR-MM-DD: ")
date2_str = input("Podaj drugą datę w formacie RRRR-MM-DD: ")

date1 = datetime.strptime(date1_str, date_format)
date2 = datetime.strptime(date2_str, date_format)

diff = date2 - date1

print(diff.days)
```

#### 6. Write a program that prompts the user for a list of numbers and returns a list of unique values.
```

while True:
    try:
        lst = input("Enter a comma-separated list of numbers: ")
        lst = lst.split(',')
        lst = [float(elem) for elem in lst]
        lst = set(lst)
        break
    except ValueError:
        print('Invalid input')
        continue

print(lst)
```

#### 7. Write a program that prompts the user for two numbers and calculates their greatest common divisor.

```
while True:
    try:

        lst = input('Enter a two numbers comma-separated: ')
        lst = lst.strip()
        lst = lst.split(',')
        num = [9,8,7,6,5,4,3,2,1]
        lst = [float(elem) for elem in lst]
        nw = []
        len(lst) == 2
        for elem in lst:
            for i in num:
                #print('4')
                if elem % i == 0:
                    nw.append(i)
                else:
                    continue
        break
                
            

    except ValueError:
        print('Invalid input. Please enter a two numbers comma-separated: ')
        continue


result = []

for i in nw:
    if nw.count(i) == 2 and i not in result:
        result.append(i)

print(max(result))

```

#### 8. Write a program that prompts the user for a list of names and returns the most frequently occurring name.
```

while True:
        try:
            lst = input('Names: ')
            lst = lst.strip()
            lst = lst.split(',')
            break
        except ValueError:
            print("Invalid input")
            continue
           

count_names = {}

for name in lst:
    if name in count_names:
        count_names[name] +=1
    else:
        count_names[name]=1
        
        
max_names = max(count_names, key=count_names.get)
print(max_names)

```
