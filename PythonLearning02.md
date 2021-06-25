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




***

