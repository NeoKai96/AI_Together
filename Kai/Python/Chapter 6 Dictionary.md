

```python
alien_0 = {'color':'green','points':5}  #字典用大括号表示，是一系列键-值对

print(alien_0)
print(alien_0['color'])               #值可以是数字，字符串，列表甚至字典
print(alien_0['points'])
```

    {'color': 'green', 'points': 5}
    green
    5
    


```python
alien_0 = {'color':'green','points':5}

new_points = alien_0['points']  #访问列表中的值
print("You just earned " + str(new_points)+ " points!")
```

    You just earned 5 points!
    


```python
#向字典添加键-值对。依次指定字典名、用方括号括起来的键和相关的值

alien_0 = {'color':'green','points':5}
print(alien_0)

alien_0['x_position'] = 0   #向字典中添加键-值对
alien_0['y_position'] = 25
print(alien_0)
```

    {'color': 'green', 'points': 5}
    {'color': 'green', 'points': 5, 'x_position': 0, 'y_position': 25}
    


```python
#创建一个空字典
alien_0={}

alien_0['color'] = 'green'
alien_0['points'] = 5
print(alien_0)
print(alien_0['color'])
```

    {'color': 'green', 'points': 5}
    green
    


```python
#改变字典中的值
alien_0 = {'color':'green'}
print("The alien is " + str(alien_0['color'])+ '.')

alien_0 = {'color':'red'}
print("The alien is now " + str(alien_0['color'])+ '.')
```

    The alien is green.
    The alien is now red.
    


```python
alien_0 = {'x_position':0, 'y_position': 25, 'speed': 'medium'}
print("Original x-position: "+ str(alien_0['x_position']))

#向右移动外星人
# 根据外星人当前位置决定将其移走多远
if alien_0['speed'] == 'slow':
    x_increment = 1
elif alien_0['speed'] == 'medium':
    x_increment = 2
else:
    x_increment = 3

# 新的位置等于老位置加上增量
alien_0['x_position'] = alien_0['x_position'] + x_increment

print("New x-position: " + str(alien_0['x_position']))
```

    Original x-position: 0
    New x-position: 2
    


```python
# 使用del删除键-值对

alien_0 = {'x_position':0, 'y_position': 25, 'speed': 'medium'}
print(alien_0)

del alien_0['x_position']
print(alien_0)
```

    {'x_position': 0, 'y_position': 25, 'speed': 'medium'}
    {'y_position': 25, 'speed': 'medium'}
    


```python
# 由类似对象组成的字典

favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }
print(favourite_language)
print('\n'+favourite_language['andrew'].title())
```

    {'jein': 'python', 'eric': 'c++', 'andrew': 'python', 'linda': 'R'}
    
    Python
    


```python
# 遍历字典。注意键值对返回顺序和存储顺序不一定相同。python只跟踪键-值对应关系，不关系键值对存储顺序
user_0 = {
    'username':'efermi',
    'first': 'enrico',
    'last': 'fermi',
    }

for key, value in user_0.items() :    #  .items()返回一对键值列表。此处
                                      # 定义的key和value可以更改为其他变量名
    print('\nKey: ' + key)
    print('Value: ' + value)
```

    
    Key: username
    Value: efermi
    
    Key: first
    Value: enrico
    
    Key: last
    Value: fermi
    


```python
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }
for name, language in favourite_language.items():
    print(name.title() + "'s favourite language is "+ 
          language.title() + '.')
```

    Jein's favourite language is Python.
    Eric's favourite language is C++.
    Andrew's favourite language is Python.
    Linda's favourite language is R.
    


```python
# 使用.keys()遍历字典中所有键。keys()返回的是一个列表
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }

for name in favourite_language.keys():
    print(name.title())
```

    Jein
    Eric
    Andrew
    Linda
    


```python
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }

for name in favourite_language:  # .keys()可以省略
    print(name.title())
    
print('\n' + str(favourite_language.keys()))
```

    Jein
    Eric
    Andrew
    Linda
    
    dict_keys(['jein', 'eric', 'andrew', 'linda'])
    


```python
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }

friends = ['eric', 'andrew']
for name, language in favourite_language.items():
    print(name.title())
    
    if name in friends:
        print(" Hi, " + name.title() + ', I see your favourite language is ' + language
            + '.')

```

    Jein
    Eric
     Hi, Eric, I see your favourite language is c++.
    Andrew
     Hi, Andrew, I see your favourite language is python.
    Linda
    


```python
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }
names = ['ash', 'andrew', 'jein', 'eric', 'linda']
for name in names:
    if name not in favourite_language:
         print(name.title() + ", please take our poll.")
   

```

    Ash, please take our poll.
    


```python
# 按顺序遍历字典中的值
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }
 
for name in sorted(favourite_language.keys()):    #使用sorted()按字母顺序进行排序，从而按顺序输出字典内键
    print(name.title() + ", please take our poll.")
```

    Andrew, please take our poll.
    Eric, please take our poll.
    Jein, please take our poll.
    Linda, please take our poll.
    


```python
# 遍历字典中的所有值。使用value(),将返回一个值列表，不包含任何键

favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }

print("The following languages have been mentioned: ")
for language in favourite_language.values():
    print(language.title())
```

    The following languages have been mentioned: 
    Python
    C++
    Python
    R
    


```python
# 集合set，类似于列表，但每个元素都是独一无二的
favourite_language = {
    'jein': 'python',
    'eric': 'c++',
    'andrew': 'python',
    'linda': 'R',
    }
print("The following languages have been mentioned: ")
for language in set(favourite_language.values()):   #将value放进一个set
    print(language.title())                         #要创建set，需要提供一个list作为输入集合
    
```

    The following languages have been mentioned: 
    C++
    Python
    R
    


```python
# set
s = set([1,2,3,4,4,4,5,5,6,7,7,8])
print(s)   #set中内容不是有序的
```

    {1, 2, 3, 4, 5, 6, 7, 8}
    


```python
# 嵌套，字典内包含列表，列表包含字典，字典包含字典等
# 字典内是不可变对象，列表内是可变对象

alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}

aliens = [alien_0, alien_1, alien_2]
for alien in aliens:
    print(alien)
```

    {'color': 'green', 'points': 5}
    {'color': 'yellow', 'points': 10}
    {'color': 'red', 'points': 15}
    


```python
# 创建一个储存外星人的空列表
aliens = []

# 创建三十个绿色的外星人
for alien_number in range(30):
    new_alien = {'color':'green', 'points': '5', 'speed': 'slow'}
    aliens.append(new_alien)

#显示前五个外形人
for alien in aliens[:5]:
    print(alien)
print('...')

print("Total number of aliens:" + str(len(aliens)))
```

    {'color': 'green', 'points': '5', 'speed': 'slow'}
    {'color': 'green', 'points': '5', 'speed': 'slow'}
    {'color': 'green', 'points': '5', 'speed': 'slow'}
    {'color': 'green', 'points': '5', 'speed': 'slow'}
    {'color': 'green', 'points': '5', 'speed': 'slow'}
    ...
    Total number of aliens:30
    


```python
for number in range(10):
    print(number)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python
# 创建一个储存外星人的空列表
aliens = []

# 创建三十个绿色的外星人
for alien_number in range(30):
    new_alien = {'color':'green', 'point': '5', 'speed': 'slow'}
    aliens.append(new_alien)
    
#将前三个外星人属性进行修改
for alien in aliens[:3]:
    if alien['color'] == 'green':
        alien['color'] = 'yellow'
        alien['speed'] = 'medium'
        alien['point'] = '10'
    elif alien['color'] == 'yellow':
        alien['color'] = 'red'
        alien['point'] = 15
        aline['speed'] = 'fast'

# 显示前五个外星人
for alien in aliens[:5]:
    print(alien)
print('...')
```

    {'color': 'yellow', 'point': '10', 'speed': 'medium'}
    {'color': 'yellow', 'point': '10', 'speed': 'medium'}
    {'color': 'yellow', 'point': '10', 'speed': 'medium'}
    {'color': 'green', 'point': '5', 'speed': 'slow'}
    {'color': 'green', 'point': '5', 'speed': 'slow'}
    ...
    


```python
# 在字典中存储列表
pizza = {
    'crust' : 'thick',
    'topping' : ['mushrooms','extra cheese'],   
}
print("You orded a " + pizza['crust'] + "-crust pizza " 
     + "with the following toppings: ")

for topping in pizza['topping']:
    print('\t'+topping.title())

```

    You orded a thick-crust pizza with the following toppings: 
    	Mushrooms
    	Extra Cheese
    


```python
favourite_languages = {
    'jen':['python','ruby'],
    'sarah':['c'],
    'edward':['ruby','go'],
    'phil':['python', 'haskell'],
}

for name, languages in favourite_languages.items():
    if len(languages) == 1:
        print("\n" + name.title() + "'s favourite language is: " + 
              '\n' +language.title())
    else:
        print("\n" + name.title() + "'s favourite language are: " )
        for language in languages:
            print(language.title())
```

    
    Jen's favourite language are: 
    Python
    Ruby
    
    Sarah's favourite language is: 
    Ruby
    
    Edward's favourite language are: 
    Ruby
    Go
    
    Phil's favourite language are: 
    Python
    Haskell
    


```python
favourite_languages = {
    'jen':['python','ruby','java'],
    'sarah':['c','c++','pin'],
    'edward':['ruby','go'],
    'phil':['python', 'haskell'],
}

for name, languages in favourite_languages.items():
    print(languages[0])#这里输出的是个矩阵？？
```

    python
    c
    ruby
    python
    


```python
# 在字典中存储字典

```


```python
# 统计列表中字母出现次数
list1 = ['a','a','b','a','b','c','d','f','f']
result = {}
s = sorted(set(list1))     #将列表转化为set，排除掉列表中的重复元素
for letter in s: 
    result[letter] = list1.count(letter)     #统计set中各元素出现次数，并加入result字典中   
print(result)

```

    {'a': 3, 'b': 2, 'c': 1, 'd': 1, 'f': 2}
    


```python
list1 = ['a','a','b','a','b','c','d','f','f','e']
result = {key: list1.count(key) for key in list1}
print(result)
```

    {'a': 3, 'b': 2, 'c': 1, 'd': 1, 'f': 2, 'e': 1}
    
