## 第八课 模块、数据结构

#### Import

```python
import module1
```

```python
from module1 import name
from modname import *
```

#### __name__属性

```python
if __name__ == '__main__':
  print("程序自身在运行")
else:
	print("我来自另一模块")
```

#### dir() 函数

```python
# 用来查看这个py文件里面有什么方法和变量的
dir('''这里是要查看的类''') # 里面是空的就是当前的类
```



## 数据结构

#### 列表推导式

- 每个列表推导式都在 for 之后跟一个表达式，然后有零到多个 for 或 if 子句

```python
# 直接把表达式写在前面
>>> vec = [2, 4, 6]
>>> [3 * x for x in vec]
[6, 12, 18]

>>> [[x, x ** 2] for x in vec]
[[2, 4], [4, 16], [6, 36]]

# 用if做过滤
>>> [3 * x for x in vec if x > 3]
[12, 18]
```

```python
# 我们对序列里每一个元素逐个调用某方法
>>> names = ['  ios', '  python ']
>>> [name.strip() for name in names]
['ios', 'python']
```

