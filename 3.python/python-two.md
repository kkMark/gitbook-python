## 第二课 Python的变量

#### 注释

```python
# 注释方式1，这种用于单行注释
"""
这个是多行注释
在三个双引号里面的都是注释
可以换行等操作
"""
```



#### 算数运算符

```python
# 在Python中，*运算符还可以用于字符串
```

| 运算符 | 说明                         |
| ------ | ---------------------------- |
| +      |                              |
| -      |                              |
| *      |                              |
| /      |                              |
| //     | 取整数                       |
| %      | 取余数                       |
| **     | 幂（次方）这个优先级是最高的 |



#### 变量

```python
# 定义方法如下
# 在python中，是不需要给变量设类型
变量名 = 值
```

```python
# 需要知道是什么类型可以通过type()函数来查看
type(变量)
```

##### 变量类型

- 数字型
  - int （整数）[int / long]
  - float （浮点型 / 小数点）
  - bool （布尔型，只有真假）
    - 非 0 即是真
    - 参数有：false[0] / true
  - complex（复合型）
    - 主要用于科学计算。例如：平面场问题、波动问题、电感电容等问题
- 非数符型
  - 字符
  - 列表
  - 元祖
  - 字典

##### 变量 - 字符之间的拼接

```python
# 字符拼接可通过 + 号进行拼接
xing = "H"
ming = "xk"
xing + ming
```