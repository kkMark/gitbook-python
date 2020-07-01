## 第五课 Python的基本变量

#### 介绍

- 在 Python 中，变量就是变量，它没有类型，我们所说的"类型"是变量所指的内存中对象的类型
- 等号（=）用来给变量赋值



#### del 语句

```python
# 用于删除对象
del var
# 可删除多个对象
del var_a, var_b
```



#### Number (数字)

```python
# 整数
number = 10
# 转换浮点
float(number)
```

#### 数学函数

| 数学函数     |                                                |
| ------------ | ---------------------------------------------- |
| abs(x)       | 返回x的绝对值                                  |
| ceil(x)      | 返回x取整数，需要导入 math 类                  |
| exp(x)       | 返回e的x次方，需要导入 math 类                 |
| fabs(x)      | 返回x的绝对值，返回的是float，需要导入 math 类 |
| floor(x)     | 返回x的下舍整数，需要导入 math 类              |
| max(.....)   | 返回取最大的值                                 |
| min(.....)   | 返回取最小的值                                 |
| modf(x)      | 返回x的小数和整数，可导入 math 类              |
| pow(x, y)    | 返回x的y次方，可导入 math 类                   |
| round(x , y) | 返回浮点数 x 的四舍五入，显示y的位数           |
| sqrt(x)      | 返回x的平方根，需要导入 math 类                |

#### 随机数函数

| 随机数函数                    | 需导入 random 类      |
| ----------------------------- | --------------------- |
| choice(x)                     | 从x随机挑选一个元素， |
| randrange (start, stop, step) | 范围内的随机值        |
| ramdom()                      | 随机值 [0 - 1]        |
| seed(x)                       | 配合随机值使用        |
| shuffle(list)                 | 对列表做随机排序      |
| uniform(x,  y)                | 生成 x - y 的随机浮点 |



#### String (字符串)

- python中的字符串用单引号 `'` 或双引号 `"` 括起来，同时使用反斜杠 `\` 转移特殊字符
- f-string 打印

```python
# 变量 [头下标:尾下标]
```

```python
# 一些String中的使用
test = 'Hello world'
print(str)						# 打印一个字符串
print(str[0:-1])			# 打印第一个到倒数第二个的所有字符
print(str[0])					# 打印第一个字符
print(str[2:5])				# 打印下标2-5的字符
print(str[2:])				# 打印从下标2开始后的字符
print(str * 2)				# 重复打印
print(str + " world")	# 拼接字符
```

#### 转义字符

| 转义字符     |            |
| ------------ | ---------- |
| \\(在行尾时) | 续行符     |
| \\\          | 反斜杠符号 |
| \\"          | 双引号     |
| \000         | 空         |
| \n           | 换行       |
| \r           | 回车       |

#### 字符串运算符

| 字符串运算符 |                                |
| ------------ | ------------------------------ |
| +            | 字符串链接                     |
| *            | 重复打印                       |
| []           | 索引                           |
| [ : ]        | 截取部分                       |
| in、not in   | 判断是否存在字段               |
| r/R          | 需要打印出来 \n 字段的时候使用 |

#### 格式化符号

| 格式化符号 |                                   |
| ---------- | --------------------------------- |
| %c         | 格式化字符及其ASCII码             |
| %s         | 格式化字符串                      |
| %d         | 格式化整数                        |
| %u         | 格式化无符号整数                  |
| %o         | 格式化无符号八进制，可在前面加#   |
| %x / %X    | 格式化无符号十六进制，可在前面加# |
| %f         | 格式化浮点型                      |
| %p         | 用十六进制格式化变量的地址        |



#### List (列表)

```python
# 变量 [头下标:尾下标]
```

```python
# 一些String中的使用
names = ["name1", "name2", "name3", "name4"]
numbers =  [123, 345]

print(names)					# 打印完整的列表
print(names[0])				# 打印第一个元素
print(names[1:3])			# 打印下标1-2的元素
print(names[2:])			# 打印从下标2开始后的元素
print(str * 2)				# 重复打印
print(str + " world")	# 拼接字符

# 新增
names.append('names5')
# 更新
names[2] = '更改名字'
# 删除
del names[2]
# 判断是否包含
'name1' in names

# 嵌套的概念 - 数组里面套数组
temps = [names, numbers]

# 常见的
# 1.获取列表数量
len(names)
# 2.统计出现的次数
names.count('要查找的内容')
# 3.在指定的位置插入
names.insert('要插入的位置（下标）', '插入的内容')
# 4.移除数组中的某个元素
names.remove('元素的类型')
# 5.清空列表
names.clear()
# 6.复制列表
names.copy()
```



#### Tuple (元组)

- 元组的内容是不可变的

```python
# 元组是使用括号的
>>> tup = ('test1', 'test2', 'test3')
# 也可以不使用括号
>>> tup = 'test1', 'test2', 'test3'

# 单个与多个的问题
tup = ('test')
type(tup) # <class 'str'>
# 加了逗号他就会变成一个元组
tup = ('test', )
type(tup) # <class 'tuple'>

# 元组的删除只能用del，而且只能整个删除
del tup

# 元组中常用的函数
# 1.数量
let(tup)
# 2.返回元组中元素最大值/最小值
max(tup) / min(tup)
# 3.强转，将一个list转成tuple
tuple(list)
```



#### Dict (字典)

- 字典用 {} 大括号来表示
- 字典都有一个对应，{ key : value }
- key 不能相同

```python
# 创建
dict = {'name' : 'XXXX', 'age' : 18}
 
# 查
print(dict['name'])
# 改/增，不存在的就是增加，存在就是修改
dict['name'] = '小明'
# 删
del dict['name']
del dict
dict.clear()
dict.pop(key)

# 常用的函数
# 1.数量
len(dict)
# 2.转换成str
str(dict)
# 3.清空
dict.clear()
# 4.将数组作为key赋值
dict.fromkeys(list, '默认值，可不填')
# 5.用于查询是否包含该字段
dict.get('name', '如果找不到就返回这里的东西')
# 6.判断是否存在key，返回True/False
key in dict
# 7.拿到所有key
dict.keys()
# 8.拿到所有value
dict.values()
# 9.追加新的字典进去
dict.update(new_dict)
# 10.删除指定的key
dict.pop(key)
# 11.随机删除字段
dict.popitem()
```



#### set (集合)

- 无序的不重复元素

- 使用 {} 或 set() 创建，创建空的需要用 set ()，因为 {} 是用于创建空的字典

```python
a = set('abracadabra')
b = set('alacazam')


# 两个集合的运算
# 1.显示 a 存在而 b 不存在的元素
a - b
# 2.显示 a、b 所有的元素
a | b
# 3.显示都包含有的元素
a & b
# 4.不同时包含于a和b的元素
a ^ b


# 集合的基本操作
# 1.添加
a.add('添加的内容')
# 1-1.添加多个
a.update({'添加的内容', '添加的内容'})
# 2.删除
a.remove('删除的内容')
# 2-1.删除，不会有错误提示
a.discard('删除的内容')
# 2-2.随机删除
a.pop()
# 2-3.清空列表
a.clear()
# 3.长度
len(a)
# 4.拷贝
a.copy()
# 5.删掉两者相同的
a.difference(b)
# 5-1.删掉两者相同的,并赋值给a
a.difference_update(b)
# 6.返回多个集合相同的元素
a.intersection(b ...)
# 7.判断是否不包含相同的元素，True / False
a.isdisjoint(b)
# 8.判断 b 中是否包含 a 的所有元素 True / False
a.issubset(b)
# 9.判断 a 中是否包含 b 的所有元素 True / False
a.issuperset(b)
# 10.移除所有相同的元素
a.symmetric_difference(b)
# 10-1.移除所有相同的元素,并赋值给a
a.symmetric_difference_update(b)
# 11.合并两个集合，相同的元素只会出现一次
a.union(b)
```

