# PythonLearning----列表和元组
PythonLearning
***
## Python列表
### 列表的创建和访问

```python
a = [1, 2.0, 'abc', [1, 2, 3], True, False] # 列表的定义
print(a)
print(a[0], a[1:6], sep='-', end='*') 
# a[1:6]为列表的切片访问，即从a[1]开始至列表的第六个元素/a[5]为止,或者理解为从a[1]开始向后选中至第（6-1）个元素
# end/sep为print函数中的参数，分别代表输出结尾打印的字符和输出元素中间的字符（默认为\n(换行)/空格' '）
print(a[3:5])
b = a[3:5] # a[3:5]为列表的切片访问，即从a[3]开始至列表的第五个元素/a[4]为止,或者理解为从a[3]开始向后选中至第（5-3）个元素
print(b, type(b))
```

```python
# 运行结果
[1, 2.0, 'abc', [1, 2, 3], True, False]
1-[2.0, 'abc', [1, 2, 3], True, False]*[[1, 2, 3], True]
[[1, 2, 3], True] <class 'list'>
```
### 列表的基本操作
#### 1.获取列表的基本信息

```python
list1 = [9, 1, -4, 3, 7, 11, 3]
print('list1的长度 =', len(list1))
print('list1中的最大值 =', max(list1))
print('list1中的最小值 =', min(list1))
print('list1中3这个元素一共出现了{}次'.format(list1.count(3)))
```

```python
list1的长度 = 7
list1中的最大值 = 11
list1中的最小值 = -4
list1中3这个元素一共出现了2次
```
#### 2.列表的改变

```python
list2 = ['a', 'c', 'd']
list2.append('e') # 在列表结尾添加字符
print('list2=', list2)
list2.insert(1,'b') # 在list2[1]处添加字符b
print('list2=', list2)
list2.remove('b') # 删除字符b
print('list2=', list2)
list2[0] = '1' # 修改list2[0]
print('list2=', list2)

# a = '123' 数组无法直接对组内单个字符进行修改
# a[0] = 'a'
# a = 'abc'
```

```python
# 运行结果 
list2= ['a', 'c', 'd', 'e']
list2= ['a', 'b', 'c', 'd', 'e']
list2= ['a', 'c', 'd', 'e']
list2= ['1', 'c', 'd', 'e']
```

```python
# 翻转列表
list3 = [1, 2, 3]
list3.reverse()
print('list3', list3)
#　排序列表 如果列表中同时包含数字和字符串类型是无法进行排序的
list4 = [9, 1, -4, 3, 7, 11, 3]
list4.sort() # 正序
print('list4=', list4)

list4 = [9, 1, -4, 3, 7, 11, 3]
list4.sort(reverse=True) # 倒序
print('list4=', list4)
```

```python
# 运行结果 
list3 [3, 2, 1]
list4= [-4, 1, 3, 3, 7, 9, 11]
list4= [11, 9, 7, 3, 3, 1, -4]
```
## Python元组
### 元组的创建和访问

```python
a = (1, 2, 3, 4) #　元组的创建
b = [1, 2, 3, 4], # 赋值后在后面加‘，’创建元组
print(a, type(a))
print(b, type(b))

print(a[1])
print(a[-1])
print(a[-2])
print(a[1:3])
print(a[1:]) # 打印从a[1]开始后面的所有项
```

```python
# 运行结果
(1, 2, 3, 4) <class 'tuple'>
([1, 2, 3, 4],) <class 'tuple'>
2
4
3
(2, 3)
(2, 3, 4)
```

### 元组的基本操作
#### 1.获取元组的基本信息

```python
tuple1 = (9, 1, -4, 3, 7, 11, 3)
print('tuple1的长度 =', len(tuple1))
print('tuple1中的最大值 =', max(tuple1))
print('tuple1中的最小值 =', min(tuple1))
print('tuple1中3这个元素一共出现了{}次'.format(tuple1.count(3)))
print('tuple1中9的索引值为', tuple1.index(9))
```

```
tuple1的长度 = 7
tuple1中的最大值 = 11
tuple1中的最小值 = -4
tuple1中3这个元素一共出现了2次
tuple1中9的索引值为 0
```
#### 2.元组的改变

​		元组无法通过像列表一样的方法改变，这点和字符串一样。

## Python列表和元组的比较

- 元组是不可变的(Immutable)Python对象，存储在固定的一块内存里；
- 列表是可变的(Mutable)Python对象，需要两块存储空间，一块固定用来存储实际的列表数据，一块可变的空间用于扩展。
- 元组创建和访问要比列表快，但不如列表灵活，不可变的或者不能改变的数据一般用元组储存。

***

