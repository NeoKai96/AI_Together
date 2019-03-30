

```python
# 列表
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles)
```

    ['trek', 'cannondale', 'redline', 'specialized']
    


```python
# 访问列表文件，列表内元素是有序的，从0开始排序

bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[0])
```

    trek
    


```python
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[0].title())
```

    Trek
    


```python
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[0].title())
print(bicycles[1])
print(bicycles[2])
```

    Trek
    cannondale
    redline
    


```python
#通过将索引指定为-1，可以返回列表最后一个值
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles[-1].title())
```

    Specialized
    


```python
# 使用列表中的值
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
message = "My first bike was a " + bicycles[0].title() + '.'

print(message)
```

    My first bike was a Trek.
    


```python
# 修改列表元素
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles[0] = 'ducati'
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['ducati', 'yamaha', 'suzuki']
    


```python
# 在列表末尾添加元素

motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles.append('ducati')
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['honda', 'yamaha', 'suzuki', 'ducati']
    


```python
# 在列表中插入元素，插入后每个后续元素右移一个位置
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles.insert(0, 'ducati')
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['ducati', 'honda', 'yamaha', 'suzuki']
    


```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles.insert(1, 'ducati')
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['honda', 'ducati', 'yamaha', 'suzuki']
    


```python
# 使用del语句删除元素,必须知道索引。被del删除的元素永久消失，无法再次使用
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

del motorcycles[0]
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['yamaha', 'suzuki']
    


```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

del motorcycles[1]
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['honda', 'suzuki']
    


```python
# 使用pop()删除列表最后一个元素，被删除的元素的值可以继续使用
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

poped_motorcycles = motorcycles.pop()
print(motorcycles)                       #一旦使用pop()，被弹出的元素就不在列表内了
print(poped_motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['honda', 'yamaha']
    suzuki
    


```python
# 使用pop()弹出特定元素
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

first_poped = motorcycles.pop(0)
print(motorcycles)                     #一旦使用pop()，被弹出的元素就不在列表内了
print(first_poped)
```

    ['honda', 'yamaha', 'suzuki']
    ['yamaha', 'suzuki']
    honda
    


```python
# 根据值删除元素，使用remove()。被remove()删除的值可以继续使用，但remove()只能删除第一个指定的值，
#若列表中有多个重复值，则需要使用循环来判断是否删除干净

motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles.remove('yamaha')
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki']
    ['honda', 'suzuki']
    


```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)

expensive = 'ducati'
motorcycles.remove(expensive)    #继续使用删除的值
print(motorcycles)
print('\nA ' + expensive.title() +' is too expensive for me' + '.')
```

    ['honda', 'yamaha', 'suzuki', 'ducati']
    ['honda', 'yamaha', 'suzuki']
    
    A Ducati is too expensive for me.
    


```python

# 对列表进行组织

```


```python
# 使用sort()对列表进行排序，按字母顺序。排序后列表无法恢复原有顺序
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)

motorcycles.sort()
print(motorcycles)


```

    ['honda', 'yamaha', 'suzuki', 'ducati']
    ['ducati', 'honda', 'suzuki', 'yamaha']
    


```python
#,向sort()传递reverse=True这个参数来逆字母顺序排序
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)

motorcycles.sort(reverse=True)
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki', 'ducati']
    ['yamaha', 'suzuki', 'honda', 'ducati']
    


```python
# 使用sorted()对列表进行临时排序，不改变列表原有排序
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print('Here is the original list: ')
print(motorcycles)

print('\nHere is the temporary sorted list:')
print(sorted(motorcycles))

print('\nHere is the original list again: ')
print(motorcycles)

```

    Here is the original list: 
    ['honda', 'yamaha', 'suzuki', 'ducati']
    
    Here is the temporary sorted list:
    ['ducati', 'honda', 'suzuki', 'yamaha']
    
    Here is the original list again: 
    ['honda', 'yamaha', 'suzuki', 'ducati']
    


```python
# sorted()逆字母顺序排列
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)
print(sorted(motorcycles, reverse = True))  #向sorted()传递reverse=True

```

    ['honda', 'yamaha', 'suzuki', 'ducati']
    ['yamaha', 'suzuki', 'honda', 'ducati']
    


```python
# 使用reverse()反转列表,永久改变列表顺序

motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)
motorcycles.reverse()
print(motorcycles)
```

    ['honda', 'yamaha', 'suzuki', 'ducati']
    ['ducati', 'suzuki', 'yamaha', 'honda']
    


```python
# 确定列表长度
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']

print(len(motorcycles))
```

    4
    


```python

```
