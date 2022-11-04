# Numpy

- 提供大量科学计算相关功能，比如数据统计，随机数生成等
- 其提供最核心类型为多维数组类型（ndarray）

### ndarray

- 描述了相同类型的“items”的集合


### NumPy ndarray 数组 和 Python list 列表的区别

Q：使用Python列表可以存储一维数组，通过列表的嵌套可以实现多维数组，那么为什么还需要使用Numpy的ndarray呢？

A：ndarray的计算速度要快很多，节约了时间

- Python list：
  - 存储的是 list 元素的引用，即内存地址，不是值
  - list 的size可以动态变化
  - 不连续内存空间
  - 每个item类型可以不一样
- NumPy ndarray：
  - 存储的是数组里元素的值
  - 创建 array时，size是固定的，一旦改变size，原来的array会被删除，重新创建一个新的array
  - 连续内存空间
  - 每个item 类型必须一致
  - 内存占用较少
  - 直接支持大量数学计算


### numpy读取文件

python中可以通过np.genfromtxt()方法读取数据然后进行后续的处理

np.genfromtxt('sars_data.txt',delimiter='/n')

### python字符串插值

```
name = 'Chris'

print(f'Hello {name}')
print('Hey %s %s' % (name, name))

print( "My name is {}".format(name))

```


### 装饰器

- 通过将现有函数传递给装饰器，从而向现有函数添加一些额外的功能
- 该装饰器将执行现有函数的功能和添加的额外功能


### Python中的实例方法、静态方法和类方法有什么区别？

- 实例方法：类创建出的具体某个对象的方法（？）

- 静态方法：使用装饰器 @staticmethod，与特定实例无关，并且是自包含的（不能修改类或实例的属性）
  - 静态方法无法修改类或实例状态，因此通常用于工具函数
  - 例如，把2个数字相加
- 类方法：接受cls参数，并且可以修改类本身


### reduce函数的工作原理

- reduce接受一个函数和一个序列
- 然后对序列进行迭代
- 在每次迭代中，当前元素和前一个元素的输出都传递给函数
- 最后，返回一个值

```
def add_three(x, y):
    print(f'x={x},y={y}')
    return x + y

li = [1, 2, 3, 5]
print(reduce(add_three, li))
```


### filter函数的工作原理

- Filter函数顾名思义，是用来按顺序过滤元素
- 每个元素都被传递给一个函数
- 如果函数返回True，则在输出序列中返回该元素
- 如果函数返回False，则将其丢弃

```

def add_three(x):
    if x % 2 == 0:
        return True
    else:
        return False
li = [1,2,3,4,5,6,7,8]

print([i for i in filter(add_three, li)])
```


### 模块（module）和包（package）有什么区别？

- 模块是可以一起导入的文件（或文件集合）：import numpy
- 包是模块的目录：from sklearn import cross_validation
