## 第九课 输入和输出

#### format() 的使用

```python
# 方法1 - 默认
print('{}网址： "{}!"'.format('百度', 'www.baidu.com'))
# 方法2 - 下标
print('{1}网址： "{0}!"'.format('www.baidu.com', '百度'))
# 方法3 - 取关键字
print('{name}网址： {site}'.format(name='百度', site='www.baidu.com'))
# 方法2、方法3可以混在一起使用
print('站点列表 {0}, {1}, 和 {other}。'.format('Google', 'Runoob', other='Taobao'))
```



#### 读和写文件

```python
# open() 将会返回一个file对象
# filename 文件名
# mode 打开文件的模式 - 查看下面的表格
open(filename, mode)
# 这个是完整版，一般不会用到，太多东西了
open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)
```

| 模式 | 说明                                   |
| ---- | -------------------------------------- |
| r    | 只用于读取文件                         |
| w    | 只用于写入文件                         |
| a    | 打开文件追加 [在尾部] [只可编辑]       |
|      | 以上三个都是单独类型，下面的是扩展类型 |
| +    | r+、w+、a+，将他们设为可读可写         |
| b    | rb、wb、ab，将他们用二进制格式操作     |
| b+   | rb+、wb+、ab+，将他们用二进制格式操作  |

```python
# 使用方法
# 创建
f = open("./test.txt", "r+")
# 写入
f.write("这里是内容，然后要String类型 \ns")
# 关闭
f.close()
```

```python
# 读取所有
f.read()
# 读取一条
f.readline()
# 读取所有，按数组来
f.readlins()
```

```python
# 查看当前的坐标
f.tell()
# 设置坐标, y 可不写
f.seek(x, y)
```

