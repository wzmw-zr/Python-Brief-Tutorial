# Python标准输入输出

## 一、标准输入`input()`

`input()`函数返回的是一个字符串，意味着使用`input()`，获得的是一个字符串，如果要求我们输入的是数字，比如整数，对输入的字符串用`int()`进行类型转换即可。

```python
a = input("input someting") # 输入字符串，括号内的是输入的提示信息
# input方法输入的都是字符串，如果需要输入的是数字的话,可以进行类型转换
b = int(input("input a interger"))
```



## 二、标准输出`print()`

`print()`函数**将所有传进来的参数值打印出来**. 它和直接输入你要显示的表达式， print() 能处理多个参数，包括浮点数，字符串。 字符串会打印不带引号的内容, 并且在参数项之间会插入一个空格, 这样你就可以很好的把东西格式化(**格式化字符串**)

使用标准输出`print()`在终端上输出信息。

```python
a = 100 * 10
print(a)
```

> Python中的所有内置数据类型都可以直接输出。

`print()`默认输入后面加一个换行符`\n`，但是我们可以指定关键字参数`end`来取消输出后面的换行，或者使用另外一个字符串来结尾。

```python
a = 100 * 10
print(a, end=",")
```



## 三、格式化字符串

Python可以使用C风格的格式化字符串，同时也有自己方便地进行格式化字符串的方法`format()`，使用方法：

```python
>>> "The sum of 1 + 2 is {0}".format(1+2)
'The sum of 1 + 2 is 3'
```

实际上就是将`1+2`的计算结果填充到{}中去，关于{}的0的含义，看下面的例子就可以明白了：

```python
>>> "{0} will {1} the American election".format("Biden", "win")
'Biden will win the American election'
>>> "{1} will {0} the American election".format("Biden", "win")
'win will Biden the American election'
```

> 之所以使用0,1...这种数字填在{}中，是因为format中的参数可以理解为是按顺序组织在一个列表中，而{}中的0,1等实际上表示的是列表中对应下标的数据。