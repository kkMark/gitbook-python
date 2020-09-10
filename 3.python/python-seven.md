## 第七课 函数

```python
# 创建函数
def 函数名(参数):
	函数内容
```

#### 参数

- 必需参数

```python
def test(str):
	print(str)
	return
  
test('测试')
```

- 关键字参数

```python
def test(str):
	print(str)
	return
    
test(str = '测试')
```

- 默认参数

```python
def test(str, content = '内容'):
	print(str)
	return
    
test(str = '测试')
```

- 不定长参数

```python
# 方式1 一个*的会以元组的方式出现
def test(arg1, *vartuple):
	print(arg1, vartuple)
	return

# 方式2 有两个**的会以字典的方式出现
def test(arg1, **var_dict):
	print(arg1, vartuple)
	return
    
test(1, 2, 3)
```



#### 匿名函数

```python
lambda [arg1 [,arg2,.....argn]]:expression
```

