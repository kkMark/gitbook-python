## 第六课 迭代器与生成器

- 迭代器有两个基本的方法：**iter()** 和 **next()**
- 字符串，列表或元组对象都可用于创建迭代器

#### 迭代器

```python
list = [1, 2, 3, 4]
it = iter(list)
print(next(it))
```

- for语句进行遍历

```python
list = [1, 2, 3, 4]
it = iter(list)
for x in it:
	print(x)
```



##### 迭代器对象

```python
# 引入 sys 模块
import sys

nums = [1, 2, 3, 4]

# 创建迭代器对象
it = iter(nums)
while True:

	# 异常判断
	try: print(next(it))
	# StopIteration 是配合迭代器一起使用
	# 迭代器没有更多的值时进入
	except StopIteration: sys.exit()
```



##### 迭代器 - 类	

```python
# 创建一个类
class MyNumbers:

   def __iter__(self):
      self.a = 1
      return self

   def __next__(self):
      x = self.a
      self.a += 1
      return x
```

- 配合 StopIteration 

```python
class MyNumbers1:

   def __iter__(self):
      self.a = 1
      return self

   def __next__(self):

      if self.a <= 20:
         x = self.a
         self.a += 1
         return x
      else:
         raise StopIteration
```

