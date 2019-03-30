

```python
#示例
cars = ['audi','honda','benze','bmw','toyota']
for car in cars:
    if car == 'bmw':   #若两边值对等，则输出True，否则返回False。大小写不同不被视为不同
        print(car.upper())
    else:
        print(car.title())

```

    Audi
    Honda
    Benze
    BMW
    Toyota
    


```python
#检查两个值是否不等
answer = 12
if answer != 10:
    print("The answer is wrong!")
```

    The answer is wrong!
    


```python
# 使用and检查多个条件
age_0 = 22
age_1 = 21
if (age_0 <=18) and (age_1>=20):
    print('Test passed')
else:
    print("Test not passed")
```

    Test not passed
    


```python
# 使用or判断多个条件
age_0 = 22
age_1 = 21
if (age_0 <=18) or (age_1>=20):
    print('Test passed')
else:
    print("Test not passed")
```

    Test passed
    


```python
#使用in检查特定值是否包含在列表中
meal = ('meat','vegetable','fruit','carbonhydrate')
if 'meat' in meal:
    print('You are not a vegan!')
```

    You are not a vegan!
    


```python
#使用not in判断特定值是否不在列表中
banned_users = ['Tod','eric','asde','wer']
user = 'marine'
if user not in banned_users:
    print(user.title()+', you can post in the froum')
else:
    print(user.title()+', you are banned!')
```

    Marine, you can post in the froum
    


```python
# 5-2
list_1 = 'word'
list_2 = 'excel'
print(list_1 ==list_2)


```

    False
    


```python
# if-else语句
age = 19
if age>= 18:
    print('You are old enough to vote!')
else:
    print('You are not old enough to vote!')
```

    You are old enough to vote!
    


```python
#if-elif-else语句，满足一个条件后跳过剩余条件
age = 10

if age<4:
    print('Your admission cost is $0.')
elif age <18:   #仅测试第一个if未通过的输入
    print('Your admission cost is $5.')
else:
    print('Your admission cost is $10.')

```

    Your admission cost is $5.
    


```python
#简化输出
age = 12

if age <4:
    price = 0
elif age<18:
    price = 5
elif age <65:
    price = 10
elif age >=65:   #if语句不一定要有else
    price = 5

print("Your admission fee is $" + str(price) +'.')
```

    Your admission fee is $5.
    


```python
#测试多个条件
requested_topping = ['mushrooms', 'extra cheese']
add_topping = []

if 'mushrooms' in requested_topping:
    add_topping.append('mushroom')
if 'pepperoni' in requested_topping:
    add_topping.append('pepperoni')
if 'extra cheese' in requested_topping:
    add_topping.append('extra cheese')

print('The toppings needed to add are: ')
for topping in add_topping:
    print(topping.title())

```

    The toppings needed to add are: 
    Mushroom
    Extra Cheese
    


```python
#5-3
alien_color = 'green'
if alien_color == 'green':
    print('You got 5 points')
    
    
alien_color2 = 'red'
if alien_color2 == 'green':
    print('You got 5 points')
else:
    print('You got 0 points')
    
```

    You got 5 points
    You got 0 points
    


```python
# 5-4
alien_color = 'green'
if alien_color == 'green':
    print("You got 5 points")
else:
    print("You got 10 points")
    
```

    You got 5 points
    


```python
# 5-5
alien_color = 'red'
if alien_color == 'green':
    print('You got 5 points')
elif alien_color == 'red':
    print('You got 15 points')
elif alien_color == 'yellow':
    print('You got 10 points')
else:
    print('You got nothing')
```

    You got 15 points
    


```python
# 使用if处理列表
#检查特殊元素
requested_toppings = ['mushrooms','green peppers','extra cheese']

for requested_topping in requested_toppings:
    if requested_topping == 'green peppers':
        print("Sorry, we are out of green pepper")
    else:
        print('Adding '+ requested_topping +'.')
        
print('\nFinish making your pizza')
```

    Adding mushrooms.
    Sorry, we are out of green pepper
    Adding extra cheese.
    
    Finish making your pizza
    


```python
#检测列表值是否为空
requested_toppings = []

if requested_toppings:   #在if中将列表作为条件表达式时，将在列表至少包含一个元素时返回True
    for requested_topping in requested_toppings:
        print('Adding '+ requested_topping +'.')
    print('Finishing making your pizza')
else:
    print('Are you shure you want a pizza?')    
```

    Are you shure you want a pizza?
    


```python
#使用多个列表
available_toppings = ['mushrooms','olives','green peppers',
                     'pepperoni','pineapple','extra cheese']

requested_toppings = ['mushrooms', 'french fries', 'extra cheese']

if requested_toppings:   #判断列表是否为空
    for requested_topping in requested_toppings:
        if requested_topping in available_toppings:
             print('Adding '+ requested_topping + '.')
        else:
            print('Sorry, we dont have ' + requested_topping +'.')
    print("\nFinished making your pizza!")
else:
    print('Please select at least one topping')
        
```

    Adding mushrooms.
    Sorry, we dont have french fries.
    Adding extra cheese.
    
    Finished making your pizza!
    


```python
# 5-8
names = ['eric', 'andrew','admin','linda','luna']

for name in names:
    if name == 'admin':
        print('Hello admin, would you like to see a status report?')
    else:
        print('Hello ' + name +', thank you for logging again.')
```

    Hello eric, thank you for logging again.
    Hello andrew, thank you for logging again.
    Hello admin, would you like to see a status report?
    Hello linda, thank you for logging again.
    Hello luna, thank you for logging again.
    


```python
# 5-9
names = []

if names:
    for name in names: 
        if name == 'admin':
            print('Hello admin, would you like to see a status report?')
        else:
            print('Hello ' + name.title() +', thank you for logging again.')
else:
    print('We need to find some users!')
```

    Please enter your name
    


```python
# 5-10
current_users = ['linda', 'andrew', 'eric', 'luna', 'dora']
new_users = ['neo','LINDA','liza','dora','boom']

for user in new_users:
    if user.lower() in current_users:    #比较时不区分大小写
        print("Your name "+ user +" is used, please select another name.")
    else:
        print('You can use this name '+user +'.')
```

    You can use this name neo.
    Your name LINDA is used, please select another name.
    You can use this name liza.
    Your name dora is used, please select another name.
    You can use this name boom.
    


```python
# 5-11
numbers = ['1','2','3','4','5','6','7','8','9']
for number in numbers:
    if number == '1':
        print('1st')
    elif number == '2':
        print('2nd')
    elif number == '3':
        print('3rd')
    else:
        print(number + 'th')
```

    1st
    2nd
    3rd
    4th
    5th
    6th
    7th
    8th
    9th
    


```python

```
