

```python
name = input("Please enter your name: ")
print("Hello, " + name + '.')
```


```python
# 创建多行字符串，是逻辑更加清晰
prompt = "If you tell us who you are, we can personalize the message you see."
prompt += "\nWhat is your name? "

name = input(prompt)
print("\nHello, " + name +'!')
```


```python
# 使用int()获取数值输入

# input直接输入是字符串形式
age = input("How old are you? ")
age

# 将input设置为数值

```


```python
# 使用int()获取数值输入
age = input("how lod are you? ")
age = int(age)
print(age>=18)
```


```python
height = input("How tall are you, in inches? ")
height = int(height)

if height >= 36:
    print("\nYou're tall enough to ride!")
else:
    print("\nYou'll be able to ride when you're a littel older.")
```


```python
# 求模运算符%，若可整除则返回零。可用于判断奇偶数
print(4%3)
print(5%3)
print(6%2)
```


```python
# 判断奇偶数
number = input("Enter a number and i will tell you it's even or odd. ")
number = int(number)

if number%2 == 0:
    print("The number is even.")
else:
    print("The number is odd.")
```


```python
# 7-1 
print("What car you are looking for? ")
car = input()

print("Let's see if i can find you a "+ car)
```


```python
# 7-3
number = input("Enter a number to see if it's 10's times. ")
number = int(number)

if number%10 == 0:
    print("It is! ")
else:
    print("It is not.")
```


```python
# while循环
```


```python
current_number = 1
while current_number <=5:
    print(current_number)
    current_number += 1
```


```python
# 让用户选择何时退出

prompt = "\nTell something and i will repeat it to you:"
prompt += "\nEnter quit to end the program. "

message = ""
while message != 'quit':
    message = input(prompt)
    print(message)
```


```python
# 隐藏掉输入的quit

prompt = "\nTell something and i will repeat it to you:"
prompt += "\nEnter quit to end the program. "

message = ""
while message != 'quit':
    message = input(prompt)
    if message != 'quit':
        print(message)
    
```


```python
# 使用标志将复杂的while判断条件简化

prompt = "\nTell something and i will repeat it to you:"
prompt += "\nEnter quit to end the program. "

active = True  #使用标志，标志应返回True或False，程序在标志为Falese时停止运行

while active:
    message = input(prompt)
    
    if message == 'quit':
        active = False
    else:
        print(message)
```


```python
# 使用break退出循环。在任何python循环中都可以使用break
prompt = "\nTell something and i will repeat it to you:"
prompt += "\nEnter quit to end the program. "

while True:   #使用while True将使程序不断运行直到遇到break
    city = input(prompt)
    if city == 'quit':
        break
    else:
        print(city)
```


```python
# 在循环中使用continue，返回到循环开头并根据条件判断是否继续执行循环
current_number = 0
while current_number <10:
    current_number += 1
    if current_number % 2 ==0:     #打印10以内的奇数
        continue
    
    print(current_number)
```


```python
# 7-4
prompt = ("Please enter the topping in your pizza: ")
prompt += ("\nEnter quit to quit. ")

active = True  # 设置标志
toppings = []   #将用户输入的topping输入一个列表
while active == True:
    topping = input(prompt)
    if topping != 'quit':
        toppings.append(topping)
        print("\nThe toppings you ordered are: " + str(toppings) + '.')
    else:
        active = False   # 用单个等号进行赋值

```

    Please enter the topping in your pizza: 
    Enter quit to quit. quit
    


```python
# 使用while循环来处理列表和字典
# 在列表之间移动元素
# 首先创建一个待验证用户列表和一个存储已验证用户的空列表
unconfirmed_users = ['alice','brian','candace']
confirmed_users = []

while unconfirmed_users:   #从未验证列表中取出用户加入验证列表中
    current_user = unconfirmed_users.pop()  #取出最后一个用户
    
    print("Verifying user: " + current_user.title())
    confirmed_users.append(current_user)
    
print("\nThe following users have been confirmed: ")
for user in confirmed_users:
    print(user.title())
```

    Verifying user: Candace
    Verifying user: Brian
    Verifying user: Alice
    
    The following users have been confirmed: 
    Candace
    Brian
    Alice
    


```python
# 删除包含特定值的所有列表元素

pet = ['cat', 'dog', 'cat','dog','goldfish','rabbit','cat']
print(pet)

pet.remove('cat') #使用remove()只能移除第一个满足条件的元素
print(pet)

#使用while删除所有满足要求的元素
while 'cat' in pet:
    pet.remove('cat')
    
print(pet)
```

    ['cat', 'dog', 'cat', 'dog', 'goldfish', 'rabbit', 'cat']
    ['dog', 'cat', 'dog', 'goldfish', 'rabbit', 'cat']
    ['dog', 'dog', 'goldfish', 'rabbit']
    


```python
# 使用用户输入来填充字典
responses = {}

polling_active = True    #创建标志

while polling_active:
    
    name = input("\nWhat is your name? ")
    response = input("Which mountain would you like to climb today? ")
    
    responses[name] = response #将答案保存在问卷中
    
    #查看是否还有人愿意参加调查
    repeat = input("是否还有人愿意参加调查？ (yes / no) ")
    if repeat == 'no':
        polling_active = False
    
# 显示调查结果
print("\n--- Poll Results ---")
for name, response in responses.items():
    print(name.title() + " would like to climb " + response +'.')
    
```

    
    What is your name? Andrew
    Which mountain would you like to climb today? li
    是否还有人愿意参加调查？ (yes / no) no
    
    --- Poll Results ---
    Andrew would like to climb li.
    


```python
# 7-8
sandwitch_orders = ["tuna", 'beef', 'firied_chicken']
finished_orders = []

while sandwitch_orders:
    order = sandwitch_orders.pop()
    
    print("I made your " + order + " sandwitch.")
    finished_orders.append(order)

print("\nYou ordered following sandwitches: ")
for sandwitch in finished_orders:
    print(sandwitch.title() + ' sandwitch')
```

    I made your firied_chicken sandwitch.
    I made your beef sandwitch.
    I made your tuna sandwitch.
    
    You ordered following sandwitches: 
    Firied_Chicken sandwitch
    Beef sandwitch
    Tuna sandwitch
    


```python
# 7-9
sandwitch_orders = ["tuna",  'pastrami', 'beef', 'pastrami', 
                    'firied_chicken', 'pastrami']

print("All pastrami sandwitchs are sold out.")

while  'pastrami' in sandwitch_orders:
    sandwitch_orders.remove('pastrami')
    
print("Sandwitches avalible: ")
for item in sandwitch_orders:
    print(item.title())
```

    All pastrami sandwitchs are sold out.
    Sandwitches avalible: 
    Tuna
    Beef
    Firied_Chicken
    


```python
# 7-10
poll = {}

active = True 

while active:
    name = input("\nWhat is your name? ")
    place = input("If you could visit one place in the world, where would you go? ")
    poll[name] = place
    
   # 询问还有没有参与调查的人
    ask = input("\nIs there anyone else to take this servey? (yes / no) ")
    if ask == 'no':
        active = False
    
for name, place in poll.items():
    print(name.title() + " would like to go to " + place + ".")
```

    
    What is your name? andrew
    If you could visit one place in the world, where would you go? america
    
    Is there anyone else to take this servey? (yes / no) no
    Andrew would like to go to america.
    
