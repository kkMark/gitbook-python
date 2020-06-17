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
| modf(x)      | 返回x的小数和整数                              |
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



#### List (列表)

```python
# 变量 [头下标:尾下标]
```

```python
# 一些String中的使用
names = ["name1", "name2", "name3", "name4"]
numbers =  [123, 345]

print(names)					# 打印完整的列表
print(name[0])				# 打印第一个元素
print(name[1:3])			# 打印下标1-3的元素
print(name[2:])				# 打印从下标2开始后的元素
print(str * 2)				# 重复打印
print(str + " world")	# 拼接字符
```


